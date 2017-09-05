## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. At a high level, what is Node?

Node is an environment to run Javascript on the server side.

2. What is Express? Why is Express similar to in the Ruby world?

Express is a framework built on top of Node to build apps in an easier way. Is similar to Sinatra in the Ruby world, because is not opinionated and nothing comes pre-built (as opposed to Rails)

3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.

```js
app.verb(`/api/v1/path`, function(request, response) {
  //receive the request, do something and return a response
})
```

4. What do we use Knex for?

We use knex to interact with the database through queries. 

5. How could you organize your code to follow the MVC design pattern in your Quantified Self project?

* Setting a server.js for our routes
* A controllers directory and their resourceController.js files to receive the request and redirect it either to a view (or status code) or to a model and return a response, 
* A models directory and their resourceModel.js files to hold all the interactions with the model (through knex)
* A views directory to hold index.js and other views

6. How do you execute raw SQL in node?

Using knex command `knex.raw('SQL QUERY ?', [variable])`

7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?

Advantages: more organized, separate responsabilities
Disadvantages: In case of changes, you have to make sure that the format of the message between the two remains the same - dependency

#### Review  

8. Describe DNS.


9. What does writing clean code mean to you?

It means it is understandable by others, it is well organized, follows single responsability (encapsulated) and DRY

10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality?

Hotels, rooms, conference_rooms
Rooms and conference rooms would have attributes such as: status (available, NA), size (amount of people), start_date, end_date (for reservation)
rooms would also have an attribute for number of beds and perks available (wifi, AC, etc)
