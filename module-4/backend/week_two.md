## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's one difference between ES5 and ES6?

ES6 introduces syntax sugar: arrow functions, Classes

2. What's the difference between asynchronous and synchronous JavaScript? 

Synchronous JS can only run one thread of operations, asynchronous JS can run multiple threads thanks to the browser through the event loop

3. What are the four pillars of Object Oriented programming?

Encapsulation, Inheritance, Polymorphism and Abstraction

4. What are some tools available in JavaScript to help you write object oriented code?

ES6: Class syntax
ES5: Objects, object constructors and object prototypes

5. What are some key concepts to be aware of when refactoring your JavaScript?

`this` keyword might change with the context, use modules for repetitive code and that way respect DRY rule.

6. What's a callback function and what are some reasons when we use/need callback functions?

Callback functions are functions that are passed through other functions as parameters to be executed later.

7. What's the scope of variables in Javascript?

Global and functional

8. What's the difference between `==` and `===` in JavaScript?
`===`is more strict than `==` because it also checks if the data type is the same.

9. Why do front end frameworks exist?

To simplify difficult tasks and provide easier ways to work.

#### Review  

10. Why do people say "HTTP is stateless"?
Because it doesn't store a `state`, it doesn't have memory of the context.

11. Describe a RESTful API.
A RESTful API is one that complies and responds to the standard verbs and standard URI's (show, index, etc)

12. What are some main characteristics of a team following an agile workflow?

Agile workflow is when a team prioritizes working on the MVP and goes through the definition, development, testing and deployment for features. They work in small sprints, usually 1 or 2 weeks, they define the MVP and iterate over it to add more features.

13. What are some advantages **and** disadvantages to using OAuth to authenticate a user?

Advantages: Easier and faster to implement, security is handled by a third party.
Disadvantages: I depend on the information that the third party is asking for/ willing to provide, if the user doesn't have an account with the third party the user can't access the application.
