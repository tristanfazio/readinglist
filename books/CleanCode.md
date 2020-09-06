# **Clean Code**

### Author
Robert C. Martin

### Online Link
https://www.amazon.com.au/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882

## **Why Am I Reading This Book?**

- VGW Associate reading list requirement
- Addiotionally, I don't just want to be a developer that can write code. I want to make this career into a craft. Something I can be proud of. This book sounds like it has a good framing, on how to be a professional in this field, and how to tend for and hone the craft of software engineering, so I am actually somewhat excited to read this book

## **Points of Interest**
---

***Chapter 1, Page 10***
-quote by *Michael Feathers*
>I could list all the qualities that i notice in clean code, but there is one overarching quality that leads to all of them. Clean code always looks like it was written by someone who cares. There is nothing more you can do to make it better... code left by by someone who cares deeply about the craft.

Quote hits a something about where I want to go with my career, I want to care about my craft, and care about improving it.

***Chapter 11, Page 171***
 *Use the simplest thing that can possibly work*

 In reference to designing systems

***Chapter 17, Page 285***

[Code Smells and Heuristics](###Chapter-17:-Code-Smells-and-Heuristics*)


- A comprehensive list of things to look out for and avoid during my career. Useful for reviewing PR's and incremental refactoring tasks.

## **Chapter Summaries**
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

- Verticle openess indicates seperation of concepts

- Verticle density indicates likeness of concepts

- Verticle distance, keep like concepts close and different concepts spaced

- Declare variables close to their usage

- Use indentation to indicate scope

### Chapter 6: *Objects and Data Structures*

- Use abstraction to hide implementations

- Avoid trainwrecks (function chaining) as it is sloppy

- Hide structure of internal objects

- Objects hide their data behind abstraction, Data Structures expose their data with no meaningful functions

### Chapter 7: *Error Handling*

- Use exceptions instead of return codes

- Use unchecekd exceptions

- Don't return null from functions

- Don't pass null into functions

- Plan your error handling

- Write meaningful messages

### Chapter 8: *Boundaries*

-  Code at boundary of API's need clear seperation and testing

- Don't depend on the details outside the boundary, depend on code you control

- Wrap boundary objects with your own for protection.

### Chapter 9: *Unit Tests*

- Three laws of TDD
    - You may not write production code until you write a failing unit test

    - You may not write more of a unit test than sufficient to fail, not compiling if failing

    - You may not write more production cocde than is sufficient to pass the recently failing test

- Test code is just as important as production code, keep it clean and maintained

- What makes a clean test? READABILITY

- Tests should be **F.I.R.S.T**
    - Fast
    - Independent
    - Repeatable
    - Self Validating
    - Timely


### Chapter 10: *Classes*

- Structure:
    - public static constants
    - private static variables
    - private instance variables

- public varaibles are seldom needed

- Like fucntions, keep them small

- Single Responsibility Principle

- Keep cohesion high (functins using variables)

### Chapter 11: *Systems*

- Construction of a system is seperate to using a system

- don't intertwine startup logic with runtime logic

- Put constrution logic into main, and have runtime logic in other parts of the application that main wires up

- Dependency Injection is powerful here

- Seperation of Concerns facilitates scaling

- Use the simplest thing that can possibly work

### Chapter 12: *Emergence*

- Simple Design Rule 1: Run all the tests
    - Run all the tests, all the time. A testable system is a verifiable system. Making testable systems pushes us to better design

- Simple Design Rule 2: Refactoring
    - Keep things clean by incrementally refactoring
    - Everytime code is written or changed, asses if it degrades teh codebase
    - Remove duplication

- Simple Design Rule 3: Expression
    - Ensure code expresses the intend of the author.
    - Express with unit tests, keeping code small, following good naming conventions

- Simple Design Rule 4: Minimize Classes and Methods
    - Sometimes pointless dogmatism results on large classes.
    - Over thinking SRP
    - Keep functions and classes as small as possible, but don't over create, keep the number of low too

### Chapter 13: *Concurrency*
- Decouples what is done from when it is done
- SRP, keep concurrency logic seperate from business logic
- Limit access of shared data
- Partition data into subsets that can be operated on by seperate threads
- Know your libray, use it's concurrency protection features
- Know your concepts
- Keep locks smalls

### Chapter 14: *Succesive Refinements*

- Big discussion with examples about how code can be blown up with changes and new features. Lot's of examples

- Code rot is expensive to clean

- Code rot destroys progress and performance

- Fix code rot before it happens by keeping things clean.

### Chapter 15: *JUnit Internals*

- pass, a discussion of JUnit

### Chapter 16: *Refactoring SerialDate*

- pass

### Chapter 17: *Code Smells and Heuristics*

***Comments***
- Inappropriate information
- Obsolete Comment
- Redundant Comment
- Poorly Written Comment
- Commented Out Code

***Environment***
- Build requires more than one step
- Tests require more than one step

***Functions***
- Too many arguments
- Output Arguments
- Flag Arguments
- Dead/Unused Function

***General***
- Multiple languages in one source file
- Obvious behaviour is unimplemented
- Incorrect behaviour at the boundaries
- Override safeties
- Duplication
- Wrong level of abstraction
- Base Classes depending on their derivatives
- Too much information
- Dead code/ Unused code
- Vertical separation
- Inconsistency
- Clutter
- Artificial Coupling
    - Eg general use enums used in specific classes forces more classes to know about them, move OUT
- Feature Envy
    - An object maniupulating it's own variables, with another objects functions
- Selector arguments
- Obscured Intent
- Misplaced Responsibility
- Inappropriate Static
- Use Explanatory Variables
- Function names should say what they do
- Understand the algorithm
- Make logical dependencies physical
- Prefer polyporphism to if/else/switch
- Follow standard conventions
- Replace magic numbers with constants
- Be precise
- Structure over convention 
- Encapsulate conditionals into functions
- Avoid negative conditionals
- Functions should do one thing
- Hidden temporal couplings 
- Don't be arbitary
- Encapsulate Boundary Conditions 
- Functions Should Descend Only One Level of Abstraction 
- Keep Configurable Data at High Levels
- Avoid Transitive Navigation

***Java***
- Avoid Long Import Lists by Using Wildcards
- Don't Inherit Constants
- Constants versus Enums
    Use the enums!

***Names***
- Choose Descriptive Names 
- Choose Names at the Appropriate Level of Abstraction
- Use Standard Nomenclature Where Possible 
    - Names are easier to understand if they relate to existing context language
- Unambiguous Names
- Use Long Names for Long Scopes 
- Avoid Encodings 
- Names Should Describe Side-Effects 

***Tests***
- Insufficient Tests
- Use a Coverage Tool!
- Don't Skip Trivial Tests 
- An Ignored Test Is a Question about an Ambiguity
- Test Boundary Conditions 
- Exhaustively Test Near Bugs
- Patterns of Failure Are Revealing
- Test Coverage Patterns Can Be Revealing
- Tests Should Be Fast 