## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?

ActiveRecord is the M in the MVC and it facilitates the way we interact with our databases. It allows us to easily access, modify and destroy data in our db, using methods that translate into sql language.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
 team.find(4).owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

```ruby
class Student << ActiveRecord::Base
  has_many :mods
  has_many :teachers, through: :mods
end
```

```ruby
class Teacher << ActiveRecord::Base
  has_many :mods
  has_many :students, through: :mods
end
```

```ruby
class Mod << ActiveRecord::Base
  belongs_to :student
  belongs_to :teacher
end
```

6. Define foreign key, primary key, and schema.

squema is the structure of our database and it's the way we describe the relationships within our database tables

primary key is the unique identifier of each row of table (the id). 

foreign key is the identifier of a row in another table that is related to our data. 

7. Describe the relationship between a foreign key on one table and a primary key on another table.

A foreign key points to an "external" table, primary key references an id within our table.

8. What are the parts of an HTTP response?
It has a head and a body. the head has a verb and a path, the body can be empty or contain additional information.

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
.all - it shows every row of that table
.count - it counts every row of that table
.max - it returns the max value
.min - it returns min value
.group().order().count() - this combination helps us group data and create a hash -> {our reference: count}


2. Name your three favorite ActiveRecord rake tasks and describe what they do.

rake db:migrate - it migrates our migrations
rake db:seed - it loads our seed into our db
rake db:rollback - it deletes our **last** migrated migrations.

3. What two columns does `t.timestamps null: false` create in our database?

created_at and updated_at (date and time)

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
```ruby
class School << ActiveRecord::Base
  has_many :teachers
end
```

```ruby
class Teacher << ActiveRecord::Base
  belongs_to :school
end
```

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
answer above

6. Give an example of when you might want to store information besides ids on a join table.

When it is relevant to the conection.

7. Describe and diagram the relationship between patients and doctors.

a doctor can have many patients, and a patient can have many doctors.

8. Describe and diagram the relationship between museums and original_paintings.

a museum can have many original_paintings and an original_painting belongs to a museum

9. What could you see in your code that would make you think you might want to create a partial?

Seeing the same code repeated throughout different models, views, etc.
