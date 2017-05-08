## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
	
	GET: it is used to retrieve information
	
	POST: used to create data in the db.
	
	PUT/ PATCH: used to update information
	
	DELETE: used to delete or destroy information

2. What is Sinatra? is a DSL that works with ruby, to develop web apps.

4. What is MVC? it means Model, Views and Controller and it is the way we organize and setup our apps in order to interact between the client and the database server.

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes? Because Rails works with this structure, and even though Sinatra is more flexible it is useful to follow this conventions.

6. What types of variables are accessible in our view templates without explicitly passing them?
Params.

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  
  ```ruby
  get '/horses' do
    name = 'Mr. Ed'
    erb :index
  end
  ```

9. What's the purpose of ERB? It's embeds ruby functionality in a webpage.

10. Why do I need a development AND test database? 

	We need a test database because we don't want to modify or delete information we might need; and we need a development database to populate and create our app.
	Basically, because we never want to touch our production db.

11. What's responsive design? It's design that adjusts to the size of the screen.

12. What is CRUD and why is it important? CRUD means Create, Read, Update and Delete. It's important because it outlines our app's functionality.

13. What does HTTP stand for? HyperText T Protocol

14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
	
	There is <% %> and <%= %>; the first one is to interpolate ruby code and the second one is to interpolate a ruby variable.

15. What's an ORM? It's Object Relational Mapping. 

16. What's the most commonly used ORM in ruby (Sinatra & Rails)? SQL, PosgreSQL

17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

	Read ----- GET ----- GET will retrieve the data from the db

	Create ----- GET + POST ----- GET will retrieve the data from the client and POST will create the data_row in the db.

	Update ----- GET + PUT/PATCH ----- GET will retrieve the data from the db and PUT will update the data_row in the db. We can use PATCH, but only for Rails.

	Delete ----- GET + DELETE ----- GET will retrieve the data from the db and DELETE will destroy the data_row in the db.

18. What's a migration? a migration is the way we create a table inside our database.

19. When you create a migration, does it automatically modify your database? No, when you create and migrate a migration you're setting the structure of a table inside the database. 

20. How does a model relate to a database? A Model is used to access and transform the data in the database.

21. What's the difference between agile workflow and waterfall method?
The difference is the way they approach a problem. When creating an app, we'll have to work on the controller, models, views and testing.
The waterfall method will work on each phase of the project and complete each phase, before moving to the next one. Agile workflow will work through iterations, doing a section of each phase, and completing each phase per functionality.
With the waterfall method, the app works when every CRUD functionality is tested and finished; with the agile workflow, the app will work as soon as one feature is finished, and you can build on that to improve it, but it doesn't need every feature to start working.

22. What is the difference between `#new` and `#create`?
`#new` creates data in the database while `#create` creates AND saves data in the db.
