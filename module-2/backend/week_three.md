## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?

`rails new app_name`

2. What do Models generally inherit from in rails?

`ActiveRecord::Base`

3. What do Controllers generally inherit from in a rails project?

`ApplicationController`

4. How would I create a route if I wanted to see a specific horse in my routes title assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

`resources :horse, only: [:show]`

5. What rake task is useful when looking at routes, and what information does it give you?

`rake routes` and it gives me the prefix, verb, URI and controller#action of each route I've created.

6. What is an example of a route helper? When would you use them?

Based on the horse example from question 4, a route helper would be `horse_path(:id)`, and it is useful to reference easily a route instead of writing the whole path each time we need to render or redirect.


7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

If I use `horse_path(:id)` is the same as if I use `/horse/:id`; if I use `horse_url(:id)` is the same as if I write `localhost:3000/horse/:id`. So, one is just the URI pattern, while the other includes the host, port and path.


8. What are strong params and why are the necessary?

Strong params are the ones we define in the controller, to limit the information from the form we allow to pass through to create a new instance.

9. What role does `form_for` play in helping us create our forms?

It's an easier way provided by rails to create forms related to our models. By using `form_for` shortcut, we avoid writing the html form and creating the relation to our database since Rails does it for us.

10. How does `form_for` know where to submit the user's input?

Depending if its rendering from a new or an edit view.

11. Create a form using a `form_for` helper to create a new `Horse`. 

```
<%= form_for(@horse) do |f| %>
	<%=f.label :name %>
	<%=f.text_field :name %>
	<%=f.submit "Create Horse" %>
<% end %>
```

12. Why do we want to validate our models?

To make sure that we are receiving all the information we need, the way we need it, keeping our database clean without useless or erroneous information.
