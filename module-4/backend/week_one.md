## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?

Using debugger, basic testing with chai and learning about how function are a scope (loops are not) and always to check if I'm returning something.

2. What are some tools to help debug JavaScript code?

debugger, console.log() or alerts. We can also use pryjs, but its better to practice with debugger and read the console. 

3. What are some tools you need in order to unit test your JavaScript?

chai

4. What is the syntax for invoking a function?

`functionName(); //put parenthesis after the function name`

5. What is CORS?

Cross-origin resource sharing. A resource does a CORS request when it requests a resource from a different domain, protocol, or port to its own. (googled this - I didn't know)

6. How do we enable CORS?

for simple requests, add to the response header: Access-Control-Allow-Origin: * (googled this - I didn't know)

7. What's `this` in JavaScript?

`this` is like `self` in ruby, in a sense that is self-referencing the object its calling it. The difference is that `this` changes depending on the context (scope) where it's being called.

8. What is Webpack and why is it useful?

Webpack allows you to use modules in the client side, so we can use different files and compresses everything into a script.

9. When/why do you want to use event delegation?

When I have elements that are dinamically added and I want to use event listeners on them. Because those elements might or might not be there, we use event delegation to call an event on an element we know is going to be present in the document and delegate it to those dinamically added elements.

10. What is a callback function?

Is when we pass a function as an argument of another function, so we can invoke it later.

11. What's `npm` and what do we use it for?

npm is a tool we can use to download/update packages for javascript.

#### Review  
12. What's the MVC design pattern? Describe each part of MVC. M = model, V = view, C = controller.

The idea is to have a structure that protects the database, so only the model can access this information, and making sure each part has single responsibility. The model is the only one that access the database, the controller receives the client's requests and redirects to the model or renders a view, and the view is in charge of showing whatever it receives from the controller.

13. What are a few ways to optimize a Rails application?

Through caching, background workers, using active record instead of ruby in the models, jobs, etc. Ideally through metrics and analyzing the specific situation.

14. What's a background worker? When would we want to use a background worker?

A background worker is a class that lets us run some functionality through redis/sidekiq. We would want to use a background worker when a specific method/feature takes too long to run. If we don't want our users to be waiting for a specific functionality to finish, we can create a background worker to run that specific functionality and notify the user when it's done.
