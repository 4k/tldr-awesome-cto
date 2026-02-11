# Improving Our Engineering Interview Process

**Source:** https://medium.com/foursquare-direct/improving-our-engineering-interview-process-106173ba25a9
**Section:** Hiring


---

Improving Our Engineering Interview Process
--
Previous Process and Motivations
Up until a year ago, Foursquare had a very typical interview process for a startup. We started with a phone call where the candidate implemented one or two simple questions in a collaborative editor. If they passed we would bring them on site for a series of hour long interviews, with mostly whiteboard coding and some system design discussion.
In terms of ensuring that the engineers we hired were great this process worked very well. Through this process, we hired a great engineering team. However, we were concerned that this process filtered out many other great engineers for reasons other than their abilities. Some possible reasons include variation between interviewers, candidate nervousness, or the unnaturalness of whiteboard coding generally. There was some evidence that this was happening since our peer companies would sometimes hire people we rejected. In addition, studies have shown there isn’t really a correlation between interview and job performance.
New Process
Today, we forgo technical phone interviews whenever possible. They’re typically unpleasant for everyone involved and we felt like the environment of a phone screen wasn’t conducive to learning about a candidate’s abilities comprehensively. Instead we give out a take-home exercise that takes about three hours. The exercise consists of three questions:
- A single-function coding question
- A slightly more complicated coding question that involves creating a data structure
- A short design doc (less than a page) on how to implement a specific service and its endpoints.
Every question we use is based on a real problem we’ve had to solve and has a preamble explaining the reason we need to solve this problem. If there is an obvious solution with a poor running time we mention it since we can’t help course-correct when the work isn’t being done live. We also provide scaffolding for the coding questions to save the candidate time.
Once we receive a take-home submission it is anonymized and put into a code review tool. The code and design doc are handed off to an engineer who does the grading. Because the submissions are anonymized the grading is done blind and reduces potential bias early in the process. For the coding questions we have a rubric which assesses the answers in terms of things like correctness, approach, and readability. The third question is used as a basis for on site discussion about systems design.
If the candidate passes, we invite them into the office for in-person interviews that include a follow-up on all take-home work already provided. For the two coding questions we have the candidate walk through the code they wrote on a laptop and explain how it works. We use any bugs or other interesting parts of their code to spark conversations, and we aren’t spending the session nit-picking. For the design question, the interviewer will pick a few parts of the design that the candidate seemed to have fleshed out and try to go in depth on them.
We still have some coding during our onsite process after the take-home, depending on the candidate’s work experience.. For all interviews we try to keep the atmosphere collaborative and conversational. Beyond coding, we talk about topics like designing a feature for a system, previous projects, previously used technologies (or new and exciting ones), and more.
Some things we learned
The biggest thing we learned is that a take home exercise based on problems we’ve had to solve is a more accurate gauge than phone screens. When candidates come on site their overall interview performance is very close to how they did on the take home, whereas with phone screens it was much more variable.
When the interviewer and candidate have the code and design already written at the start of the interview they are able to dive deeper and have more insightful discussions. It has a more natural feel and flow than live coding interviews because it more closely mirrors what our engineers do in their day-to-day.
In an early version of the process we tried to have the candidate find and explain their bugs. It was much more difficult to conduct for the interviewer and led to less consistent assessments and worse candidate experiences than the “code review” style mentioned above.
Because we start the interview process with something that is familiar, the changes we made help reduce the chance of nervousness and serve as a great warmup to the rest of the day. A bonus is that the feedback from candidates has been overwhelmingly positive. They especially seem to enjoy how interactive this interview is and that they can have a technical conversation to evaluate Foursquare.
In terms of the content of the take-home, early versions asked the candidate provide tests for their code. The tests provided basically no extra signal and were adding significantly to the time it took to complete so we eliminated them. We also added scaffolding to save the candidate time. It also had the bonus of making it much easier to run our auto-tests.
Next
We know the process still isn’t quite perfect, but we’re happy to have taken this first step. Foursquare’s other departments are starting to implement this into their interviewing process after seeing our successes! We’re excited to continue working on our process because we’re determined to build a great team and do it in the best way possible.
— Jeff Jenkins (@JeffWJenkins) and David Park (@dotdpark)
P.S. we’re hiring!