# Falsehoods Programmers Believe About Names

**Source:** https://www.kalzumeus.com/2010/06/17/falsehoods-programmers-believe-about-names/
**Section:** Related stuff

---

## Key Insights

- Names are far more complex than any system accounts for - there is no such thing as a "canonical" name format
- People can have multiple valid full names they go by simultaneously (author acknowledges 6 different versions)
- Names change unpredictably - not just at marriage/divorce but at any time for any reason
- Character encoding assumptions fail globally - names use ASCII, Unicode, mixed character sets, numbers, all caps, all lowercase
- First/last name separation is culturally biased - many cultures don't follow this pattern
- Name uniqueness is myth - millions can share identical names, especially in China/Asia
- Database schemas with `first_name`/`last_name` columns are fundamentally broken
- Systems that validate names against "acceptable characters" are discriminatory by design
- Two operators entering the same person's name will produce different strings due to spelling variations
- Some people have no names at all in traditional Western sense
- Dictionary-based profanity filters will inevitably block legitimate names
- Name assignment timing varies - not always at birth, sometimes years later
- Global systems must handle naming conventions from every culture simultaneously
- Any transformation algorithm for names will cause data loss

## Bottom Line

Every assumption developers make about names is wrong, and robust systems must accept any string a person claims as their name without validation or transformation.