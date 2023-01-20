# My Coding Standards

## Conventions

1. Use lint and some kind of style checker.
2. Never arbitrarily disable a lint rule. If there is any inconsistency between the rule and the design style, the rule should be revised.
3. Use descriptive names, even if they are long.
    
    Avoid abbreviations, especially if the variable is used in a broad context. In short contexts it *may* be acceptable (eg a lambda function).
    
    Avoid ambiguities.
    
    **Think carefully before assigning a name**.
    
    ```jsx
    const c = 0; // 👎
    const userActivityCounter = 0; // 👍
    ```
    
    ```jsx
    const admins = usersList.filter(u => u.isAdmin()); // 👍 but let's avoid it
    ```
    
    ```jsx
    const projectData = {};
    const dataProject = {}; // 👎 if they are in the same context
    ```
    
4. Variable names must be nouns, as they represent things.
    
    ```jsx
    const user = {};
    const counter = 0;
    const houses = [];
    ```
    
5. Function names must contain verbs as they represent actions.
    
    ```jsx
    function saveFormChanges() {}
    function handleKeyboardEvent() {}
    function createNewTemplate() {}
    ```
    
6. Functions that return logical values in general can use `is` and `has`.
    
    ```jsx
    function isActive() {}
    function hasRole(role) {}
    ```
    
7. Comments are rarely needed. The code must be clear and expressive enough to be understood.
8. Never submit "magic numbers" to the repository.  
[Refactoring.com > Replace Magic Literal](https://refactoring.com/catalog/replaceMagicLiteral.html).
9. Never commit commented code to the repository. Use branches.
10. Remove any commented code you find if you make sure that is wasn't commited by accident.
12. **In the absence of a Feature Flags system**, never push unused code to the repository as it can confuse your team.
12. **In the absence of a Feature Flags system**, remove any code that you ensure is unused.
13. Code lines should not exceed *100* characters (It's hard to find a criterion to define the exact number. It can be 72, 80, 120...).
14. Respect code indentation.

## Clean Code Summary

[Summary of 'Clean code' by Robert C. Martin @github.com/wojteklu](https://gist.github.com/wojteklu/73c6914cc446146b8b533c0988cf8d29)

[Clean Code concepts adapted for JavaScript @github.com/ryanmcdermott](https://github.com/ryanmcdermott/clean-code-javascript)

## Good Practices

1. Avoid repetitions but be careful with coupling.  
[DRY is about Knowledge @verraes.net](https://verraes.net/2014/08/dry-is-about-knowledge/)
2. Split the code into short functions, always focused on a single action, even if these functions are only used in one place. Too many loops and conditions in a function is a symptom that it needs to be split.  
[Cyclomatic complexity @wikipedia.org](https://en.wikipedia.org/wiki/Cyclomatic_complexity)
3. Whenever possible, implement pure functions without side effects. Side effects make code extremely difficult to understand, test, and debug.  
[Pure vs Impure Functions @dev.to/sanspanic](https://dev.to/sanspanic/pure-vs-impure-functions-50aj)
4. Too many parameters in a function (or props in a component) is a signal that the function is poorly designed and needs refactoring.  
[▶️ Clean Code III: Functions - Robert C. Martin](https://vimeo.com/channels/1111213/12643301)
5. Avoid abstract classes. Favor composition over inheritance.  
[Composition vs. Inheritance: How to Choose? @thoughtworks.com](https://www.thoughtworks.com/insights/blog/composition-vs-inheritance-how-choose)
6. Refactor your new code before pushing it to the repository.  
[refactoring.com/catalog/](https://refactoring.com/catalog/)  
[refactoring.guru/refactoring](https://refactoring.guru/refactoring)  
[sourcemaking.com/refactoring](https://sourcemaking.com/refactoring)
7. Always try to leave the code better than you found it.  
8. Think hard about the task to be performed, the problem to be solved.  
[▶️ Hammock Driven Development - Rich Hickey](https://www.youtube.com/watch?v=f84n5oFoZBc)
9. Count on change and always think about the future.  
    > If someone else needs to maintain this code six months from now, will they be able to understand what they did and change the code easily?
10. What makes software easy to change is its structure. Structure is more important than behavior.  
    Software must be *soft*.  
    [What is the value of software development? @medium.com/@mvidaurre](https://medium.com/@mvidaurre/what-is-the-value-of-software-development-c90ac18b786d)  
    [Clean Architecture — Two values @medium.com/@stoltmanjan](https://medium.com/@stoltmanjan/clean-architecture-two-values-f93f399de4e)  
    > Working software that cannot be modified tends to become obsolete and disappear. Software open to change, even if defective, can work again.

## S.O.L.I.D. Principles

[▶️ Uncle Bob SOLID principles](https://www.youtube.com/watch?v=zHiWqnTWsn4)

[▶️ The S.O.L.I.D. Principles of OO & Agile Design - Uncle Bob Martin](https://www.youtube.com/watch?v=t86v3N4OshQ)

SRP: The Single Responsibility Principle.

OCP: The Open Closed Principle.

LSP: The Liskov Substitution Principle.

ISP: The Interface Segregation Principle.

DIP: The Dependency Inversion Principle.

## Component Principles

[▶️ Robert C. Martin: Principles of Component Design](https://vimeo.com/68236438)

## Coesion Principles

REP: The Release-Reuse Equivalence Principle

CCP :The Common Closure Principle

CRP: The Common Reuse Principle

## Coupling Principles

ADP: The Acyclic Dependencies Principle

SDP: The Stable Dependencies Principle

SAP: The Stable Abstractions Principle

## Clean Architecture

[DDD, Hexagonal, Onion, Clean, CQRS, … How I put it all together @herbertograca.com](https://herbertograca.com/2017/11/16/explicit-architecture-01-ddd-hexagonal-onion-clean-cqrs-how-i-put-it-all-together/)

[Ready for changes with Hexagonal Architecture @ netflixtechblog.com](https://netflixtechblog.com/ready-for-changes-with-hexagonal-architecture-b315ec967749)

[Introducing Domain-Oriented Microservice Architecture @eng.uber.com](https://eng.uber.com/microservice-architecture/)
