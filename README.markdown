# Ruby on Rails Tutorial: demo application

This is the 2nd app for [*Ruby on Rails Tutorial: Learn Rails by Example*](http://www.railstutorial.org) by [Michael Hartl](http://www.michaelhartl.com). I'm writing about it here as an exercise to see what I've learned. haha. 

This demo app is in the second chapter. After reading many warnings about how the rest of the book will teach us how do build things from the ground up, we created a demo app using scaffolding, and learned about these things: 

1.  The Model-view-controller (MVC) architectural pattern([1](http://www.railstutorial.org/book#sec:mvc)) -- we created User and Micropost models, which get called by the controller, and after the controller gets stuff from the models, it passes that stuff to the view, which passes back some html.([2](http://www.railstutorial.org/chapters/a-demo-app#sec:mvc_in_action)) I think the controller and the view guys were generated automatically. I learned some conventions in the scaffolding system: *models* are singular (so the model is called 'User') while *controllers* and *resources* are plural (so the 'User' controller gets called 'Users' ...uh, i think)

2.  For relational databases, there's  [CRUD](http://en.wikipedia.org/wiki/Create,_read,_update_and_delete) -- create, read , update, delete. The four fundamental HTTP request methods are: post, get, put, and delete. We learned about REpresentational State Transfer (REST), which says that most application components are modeled as resources that can be created, read, updated, and deleted.([3](http://www.railstutorial.org/chapters/a-demo-app#sidebar:REST))

3.  We messed around with creating, looking at, deleting, and editing users and microposts via a web browser on localhost. 

4.  We added length validation to the micropost's content field! ([4](http://www.railstutorial.org/chapters/a-demo-app#sec:putting_the_micro_in_microposts)) We also told the User model that a user has many microposts, and we told the Micropost model that it belongs to a user. Then we opened the Ruby console and displayed all the microposts associated with the first user (but I still don't know how to look at any from any other user, because it uses User.first oddly).

5.  We learned about Inheritance. 

the 'User' and 'Micropost' classes are \< 'ActiveRecord::Base', which is the base class for models provided by ActiveRecord. That's how our model objects get the ability to communicate with the database, treat the database columns as Ruby attributes...([5](http://www.railstutorial.org/chapters/a-demo-app#sec:inheritance_hierarchies))
	
UsersController and MicropostsController are both \< ApplicationController, which is itself \< ActionController::Base, getting the ability to manipulate model objects, filer inbound HTTP requests, and render views as HTML. Since all Rails controllers inherit from ApplicationController, rules defined in the Application controller automatically apply to every action in the application.([6](http://www.railstutorial.org/chapters/a-demo-app#fig:demo_controller_inheritance))

6. Then we pushed it to github and deployed to Heroku. <http://blazing-wind-36.heroku.com>!!!!!!!!!!


 
	this is a code block. 
	i think markdown is pretty cool!
	
