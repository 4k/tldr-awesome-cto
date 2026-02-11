# How I Write Tests

**Source:** https://blog.nelhage.com/2016/12/how-i-test/
**Section:** Architecture


---

The longer I spend as a software engineer, the more obsessive I get about testing. I fully subscribe to the definition of legacy code as “code without an automated test suite.” I’m convinced that the best thing you can do to encourage fast progress in a test suite is to design for testing and have a fast, reliable, comprehensive test suite.
But for all that, I’ve never really subscribed to any of the test-driven-development manifestos or practices that I’ve encountered. I don’t believe in religiously writing tests before code, or swear by any particular structure for tests.
I do try to write a lot of tests, these days, though, and I do try to write my code with tests in mind. And I’ve come to realize that my approach could be thought of as a test-driven-development philosophy. Here’s how I think about code and testing, especially in green-field systems or components.
Work module-at-a-time 🔗︎
(My previous post covers a lot of how I think about this)
As I explore how to structure a new project, I think about how to structure it into separable components, guided by the question of “How can I design units that are testable with as few dependencies as possible?”
As I work on each module, I try to write tests for the code in that module before I move on.
I rarely write the tests before the code. Except for the simplest cases, I often don’t know the details of the implementation and interfaces I’m writing until I’ve started working on them and experimented with a few approaches. If writing the tests (which are, themselves, clients of the interface!) helps me feel out the interfaces, I might do so, but it’s certainly not a rule.
However, I do try to write a module and its tests together, and – as much as possible – complete both before moving on to another module. This practice helps ensure that my modules are testable (and minimally coupled with the rest of the system), as well as to ensure ongoing test coverage.
This rule (and in fact, none of the rules I list here) isn’t a hard and fast rule for me. I cheat sometimes. But I’ve found this approach to be a valuable heuristic.
Avoid running main
🔗︎
When developing a new project, or adding a feature, there’s a very strong instinct to start with manual testing – to run the binary and test the new feature by hand.
I try very hard to resist this urge.
Instead, as soon as I’ve added a feature, if I find myself itching to try it out by hand, I’ve learned to recognize that urge, pause, and step back and write an automated test covering whatever behavior I was about to execute by hand.
Manual testing is often quick and easy and satisfying – you can directly test your application, one can see the results immediately on your screen, and one can interact with the application “for real”, instead of in the sometimes-awkward scripted/mocked mode of unit tests. It’s a very natural instinct.
However, it’s also largely-wasted effort! A manual test only verifies the current state of the code base. As soon as you make a change, you’ve started to invalidate the results. If, however, you take the effort to encode the test in code as an automated test, it continues to be valid indefinitely into the future.
Build tools for testing 🔗︎
Of course, it is often genuinely substantially easier to test your application by hand than to write a test. Clicking is much simpler than trying to reason about coordinates. Entering input and getting feedback interactively is easier than encoding an entire transcript up front by thinking hard.
If testing your application in code is hard or frustrating, it’s worth the effort to invest in your own testing tooling to make it easier! Tests are an important part of your codebase, and you wouldn’t skip important features just because they were hard!
Here are some concrete techniques I’ve found and try to use regularly to make writing tests easier and more productive.
Write lots of fakes 🔗︎
No one seems to agree quite on the boundaries between “fakes”, “mocks”, “stubs”, and various other testing concepts. But I’m going to use the term “fake” as I picked it up from a great PyCon talk, which is a standalone implementation of a component’s interface that is reusable between multiple tests, and that is independently testable on its own. (That’s a good talk, by the way, that very much influenced my thinking. It’s worth a watch.)
In some cases, a fake can be a near-complete in-memory implementation of a backend. For instance, if your application depends on S3, you can probably implement an in-memory blob store that implements your internal S3 interface, and then re-use it everywhere in your tests. As another concrete example, during testing, Django replaces its internal email implementation with an in-memory email outbox, letting you run your code unchanged and then observe the output.
If your interface is too complex, you can still provide a “programmable” fake that lets tests configure or plug in its behavior in appropriate ways, instrucing it how to respond to inputs. Such a fake still provides value by structuring testing, and sharing lower-level, ancillary details of implementing the interface.
The “sarama” Go Kafka client implements such a programmable fake kafka broker, which is used repeatedly in the library’s own tests, and can also be used by consumers wishing to construct more end-to-end tests.
Anytime you find yourself stubbing out an external in an ad-hoc basis, it’s worth stepping back and asking if you should be writing a reusable fake. It’s more effort up front, but it will decrease the cost of writing future tests, and increase your tests' maintainability, both vital goals.
Design miniformats for test input and output 🔗︎
Often when writing tests, you want to construct either a domain object or some input to your system with particular properties – certain contents, a certain bit pattern, whatever. It’s very easy to find yourself writing long sequences of code to construct objects, or copying around opaque representations of internal data structures.
One powerful technique can be to design and implement a small textual format for representing your data (either internal state objects, or structured input), that is easily human readable and writable. Then, augment your tests and application so that you can easily input or print objects using this format. Now, when you need an object of a specific shape, you can take this easy textual representation, edit it to match what you need, and start your testing from there.
You can often use this format to provide a way to make manual testing more reproducible. Construct some specific input or internal state manually, and then configure the application to dump it in your miniformat. Now you can easily encode that into a test and replay from wherever you were.
My favorite example of this technique is David Benjamin’s DER ASCII project. David is half of the BoringSSL project, and as such spends a lot of time dealing with X.509 certificates and messages, which are encoded in ASN.1 DER, a moderately gnarly binary format. He wrote DER ASCII to provide a simple textual representation of these structured binary strings, allowing him to represent, generate, and modify them for testing purposes much more easily than he otherwise could.
Design a testing minilanguage or “zoo” 🔗︎
Often, it’s worth going one step forward and building a completely data-driven test harness that lets you express common types of test cases entirely as data files in a directory, without adding any additional code. Done right, this lets you add new test cases directly in a familiar format, and even directly translate bug reports or interactive tests into test cases.
(A coworker calls this pattern a “zoo”, because you get one directory containing all of your exotic animals, and I’ve adopted that nickname)
This technique is well-known among compiler developers (probably because compilers have the luxury of a very clear input format: simple text files); Take a look at a sample gcc test case. You needn’t read it in detail, but skim over it, and note some key techniques and details:
- This is a self-contained test case. Someone created this test by adding this file, which is in a format very familiar to any GCC developer (C source), and by doing no additional work (e.g. there’s no secondary list of these, or configuration)
- Note the
{dg-* …}
comments. In order to make these tests self-contained, and able to express many varieties of tests (correctness, error messages, warnings, etc), GCC developers have built a custom annotation/directive system (what I call a “testing minilanguage”) to instruct the test harness how to interpret this test case, and what to check for.
Building a runner for these test cases is a bit of upfront investment, but it’s well worth it; By making it easier to write tests, you’ll ensure that you and other contributors write more tests, and your future selves (and other future developers!) will thank you for the effort.
This technique is easiest for programs with simple self-contained
textual inputs (such as compilers), but it can be adopted more
widely. At my work, I worked on an internal HTTP proxy application; We
built out a test harness so that we could ultimately paste entire HTTP
requests and the expected responses into files, and perform automated
testing by replaying and comparing those. This required stubbing out
various pieces of entropy and having a “standard” well-known initial
database state for these tests, but the end result was very easy
regression testing – most bugs we found could be encoded as
regression tests by just copy/pasting from logs and/or tcpdump
with
some slight modification.
Regression tests, Regression tests, Regression tests 🔗︎
My final, and perhaps more important, advice is to always write regression tests. Encode every single bug you find as a test, to ensure that you’ll notice if you ever encounter it again.
This doesn’t have to just mean “bugs reported by a user” or anything similar; Any bug you find in the course of development is worth writing a test for. Even if you find yourself half way into typing a line of code, realize you’ve made a mistake, and backspace half the line: Pause, and ask yourself “If I had made that mistake, is there a test I could have written to demonstrate it?”
The goal is, essentially, to ensure a ratchet on the types of possible bugs in your system. There are probably nigh-infinitely many bugs you could write, but the set of desired behaviors of your system is relatively finite, and the set of bugs you’re likely to write is similarly limited, and if you turn every bug into a test on one of those behaviors, you’ll eventually converge on testing for most of the important failure modes of your system.
At least, that’s the optimistic take. Even if it doesn’t converge, though, there’s a lot to be said for only having any specific bug once, ever.