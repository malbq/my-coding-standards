# My Coding Standards

## Conventions

1. Use lint e algum tipo de style checker.
2. Nunca desabilite uma regra de lint arbitrariamente. Se houver alguma incoerência entre a regra e o estilo do projeto, a regra deve ser revisada.
3. Use nomes descritivos, mesmo que sejam longos.
    
    Evite abreviações, principalmente se a variável for usada em um contexto amplo. Em contextos curtos *pode* ser aceitável (p. ex. uma função lambda).
    
    Evite ambiguidades.
    
    **Pense bem antes de atribuir um nome**.
    
    ```jsx
    const c = 0; // 👎
    const userActivityCounter = 0; // 👍
    ```
    
    ```jsx
    const admins = usersList.filter(u => u.isAdmin()); // 👍 mas vamos evitar
    ```
    
    ```jsx
    const projectData = {};
    const dataProject = {}; // 👎 se estiverem no mesmo contexto
    ```
    
4. Nomes de variáveis devem ser substantivos, pois representam coisas.
    
    ```jsx
    const user = {};
    const counter = 0;
    const houses = [];
    ```
    
5. Nomes de funções devem conter verbos, pois representam ações.
    
    ```jsx
    function saveFormChanges() {}
    function handleKeyboardEvent() {}
    function createNewTemplate() {}
    ```
    
6. Funções que retornam valores lógicos em geral podem usar `is` e `has`.
    
    ```jsx
    function isActive() {}
    function hasRole(role) {}
    ```
    
7. Comentários são raramente necessários. O código deve ser claro e expressivo o suficiente para ser entendido.
8. Nunca envie "números mágicos" para o repositório.  
[Refactoring.com > Replace Magic Literal](https://refactoring.com/catalog/replaceMagicLiteral.html).
9. Nunca envie código comentado para o repositório.
10. Remova todo código comentado que encontrar.
12. **Na ausência de um sistema de Feature Flags**, nunca envie código não usado para o repositório.
12. **Na ausência de um sistema de Feature Flags**, remova todo código não usado que encontrar.
13. Linhas de código não devem passar de *100* caracteres (É difícil achar um critério pra definir o número exato que pode ser 72, 80, 120...).
14. Respeite a indentação.

## Clean Code Summary

[Summary of 'Clean code' by Robert C. Martin @github.com/wojteklu](https://gist.github.com/wojteklu/73c6914cc446146b8b533c0988cf8d29)

[Clean Code concepts adapted for JavaScript @github.com/ryanmcdermott](https://github.com/ryanmcdermott/clean-code-javascript)

## Good Practices

1. Evite repetições mas tome cuidado com acoplamento.  
[DRY is about Knowledge @verraes.net](https://verraes.net/2014/08/dry-is-about-knowledge/)
2. Divida o código em funções curtas, sempre focadas em uma única ação, mesmo que essas funções sejam usadas em apenas um lugar.
Muitos laços e condições em uma função, são um sintoma de que ela precisa ser dividida.  
[Cyclomatic complexity @wikipedia.org](https://en.wikipedia.org/wiki/Cyclomatic_complexity)
3. Sempre que possível, implemente funções puras, sem efeitos colaterais.
Efeitos colaterais tornam o código extremamente difícil de entender, testar e debugar.  
[Pure vs Impure Functions @dev.to/sanspanic](https://dev.to/sanspanic/pure-vs-impure-functions-50aj)
4. Muitos parâmetros em uma função sinalizam que a função foi mal concebida e necessita refatoração.  
[▶️ Clean Code III: Functions - Robert C. Martin](https://vimeo.com/channels/1111213/12643301)
5. Evite classes abstratas. Favoreça composição ao invés de herança.  
[Composition vs. Inheritance: How to Choose? @thoughtworks.com](https://www.thoughtworks.com/insights/blog/composition-vs-inheritance-how-choose)
6. Refatore o código novo antes de enviar para o repositório.  
[refactoring.com/catalog/](https://refactoring.com/catalog/)  
[refactoring.guru/refactoring](https://refactoring.guru/refactoring)  
[sourcemaking.com/refactoring](https://sourcemaking.com/refactoring)
7. Procure sempre deixar o código melhor do que você encontrou.  
8. Pense bastante sobre a tarefa a ser executada, sobre o problema a ser resolvido.  
[▶️ Hammock Driven Development - Rich Hickey](https://www.youtube.com/watch?v=f84n5oFoZBc)
9. Conte com a mudança e pense sempre no futuro.
    
    > Se outra pessoa precisar dar manutenção nesse código daqui a seis meses, vai conseguir entender o que foi feito e alterar o código com facilidade?
10. O que torna um software fácil de mudar é sua estrutura. Estrutura é mais importante do que comportamento.

    Software deve ser *soft*.  
    [What is the value of software development? @medium.com/@mvidaurre](https://medium.com/@mvidaurre/what-is-the-value-of-software-development-c90ac18b786d)  
    [Clean Architecture — Two values @medium.com/@stoltmanjan](https://medium.com/@stoltmanjan/clean-architecture-two-values-f93f399de4e)
    
    > Um software funcional que não pode ser modificado tende a ficar obsoleto e desaparecer. Um software aberto a mudanças, ainda que defeituoso, pode voltar a funcionar.

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