# **Clean Code**

### Author
Robert C. Martin

### Online Link
https://www.amazon.com.au/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882

## **Why Am I Reading This Book?**

- VGW Associate reading list requirement
- Addiotionally, I don't just want to be a developer that can write code. I want to make this career into a craft. Something I can be proud of. This book sounds like it has a good framing, on how to be a professional in this field, and how to tend for and hone the craft of software engineering, so I am actually somewhat excited to read this book

## **TL;DR Summary**
---

thoughts

## **Points of Interest**
---

Chapter 1, Page 10
-quote by *Michael Feathers*
>I could list all the qualities that i notice in clean code, but there is one overarching quality that leads to all of them. Clean code always looks like it was written by someone who cares. There is nothing more you can do to make it better... code left by by someone who cares deeply about the craft.

Quote hits a something about where I want to go with my career, I want to care about my craft, and care about improving it.

## **Notes**
---

notes

## C**hapter Summaries**
---

### Chapter 1: *Clean Code*

Bad code produces knots. Knots are hard to unpick. As business wants new features more knots need to be added to avoid the previous.

Reduces dev team speed and productivity

*Leave the campground cleaner than you found it*

### Chapter 2: *Meaningful Names*

- Use intention revealing names

- Avoid disinformation

- Use pronounceable names

- Use searchable Names

- Avoid encodings
    eg no I preceeding interface, 

- Class Names should be nouns

- Method names should be verbs

Naming requires good descriptive skills and cultural background

### Chapter 3: *Functions*

- Keep them small

- Do one thing

- One level of abstraction per function

- Switch statements should be avoided
    - they are hard to keep small
    - hard to maintain as code grows new types need to be added
    - when you can, use a switch statement buried in a factory and utilise interfaces.
    - this ensures the function does "one" thing, returning the appropriate type, and that type handles it's own functions.

- Flag argumants indicate a function is doing more than one task

- Argument amounts

    - Niladic, zero arguments

    - Monadic, 1 argument

    - Dyadic, 2 arguments

    - Triad, 3 arguments *avoid*

    *where possible, group like arguments into objects to reduce complexity

### Chapter 4: *Comments*

- Comments decay over time, code changes, comments don't get updated.

- Inaccurate commetns are worse than no comments at all, they are misleading.

- The remedy is to write code that is self descriptive and understandble, reducing the need for comments

- Only use comments if you have to.

### Chapter 5: *Formatting*


