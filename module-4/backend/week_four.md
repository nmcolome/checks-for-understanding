## Week Four - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's your favorite project management tool?

Waffle, because is very simple, is connects to github immediately and updates issues and tracks PRs.

2. Why do we create staging environments?

To have an environment where we have the ability to experiment and make mistakes (like development) but with the same resources and conditions of production; so we can see how our code behaves under real life conditions and constraints.

3. What are the characteristics of a good README (in your opinion)?

It has a brief description, the stack (and versions!) that it uses, instructions for download, setup, how to use it (if necessary), on how to submit issues or how to contact the team. If it's open source, how to submit PR. 
In general, it should be brief, clear and have examples.

4. What's one main improvement you're going to make to your code regarding accessibility issues?

I want my frontend to be very clean and intuitive so it doesn't have many distractions, make sure you can tab around and read it through a screen reader to make sure is as understandable as possible.

5. What are some basic security concerns to be aware of when building applications?

The most basic and common is SQL or Javascript injection and learning how to protect ourselves.

6. Why is continuous integration helpful/important?

It's important because it helps us make sure that whatever code we're pushing is not breaking anything.

7. What are some continuous integration tools?

Travis CI, Circle CI, Semaphore

#### Review  

8. What are some characteristics of "good" git workflow?

Commit every 15min or do atomic commits (don't wait too much to commit), have clear descriptive commits, don't merge your own work, use a branch for every feature.

9. What are the four fundamental concepts of object oriented programming?
Abstraction
Polymorphism
Inheritance
Encapsulation

10. What's a module in Ruby and what's the difference between a class and a module?

A class represents the blueprint for an object, a module is like a container for methods that are common between different classes (SRP principle). Differences are: a class has inheritance and you need to instantiate a class. To use a module you have to require it in a class, and it's functionality is to namespace methods or include additional methods to that class. 
