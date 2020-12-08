# rent_payment_API
This is an API to register rent payments 

For this project I will use the MVC (Model-View-Controller) which is a pattern used to help organize and structure code. Specifically, most code will be classified as a model, view, or controller. I will organize the code into packages based on its "layer" or in other words, I package all the views together, all the controllers together, and so on. This is by far the most common layout for MVC.

MVC is a pretty natural evolution from a flat-structured application where we often break our code into a database, handler, and rendering layer anyway. All three of these map pretty nicely to models, controllers, and views.

## Models
* Their primary responsibility is interacting with your application's data. This typically means communicating with your database, but it could also mean interacting with data that comes from other services or APIs. It might also mean validating or normalizing data.
* The models package includes all the interactions with the database.
* The models package should contain pretty much all of your code related to your data storage. That includes database-specific models, validations, normalizations, etc.
* Here are a few examples of logic I might expect to find in a models package:
1. Code that defines the User type as it is stored in the database.
2. Logic that will check a user's email address when a new user is being created to verify that it isn't already taken.
3. If your particular SQL variant is case sensitive, code that will convert a user's email address to lowercase before it is inserted into the DB.
4. Code for inserting users into the users table in the DB.
5. Code that retrieves relational data; eg a User along with all of their Reviews.

* In models cannot be anything like return errors with Http status codes or HTML responses or something like that.

## Views
  Are responsible for rendering Data. Our view could just as easily handle rendering XML, JSON, or other data types. The important thing to remember is that the code in a view should have as little logic going on as possible; instead, it should focus entirely on displaying data.

## Controllers
  Air traffic controllers are the people that inform each plane at an airport where to fly, when to land, and on which runway to land. They don’t actually do any piloting, but instead are in charge of telling everyone what to do so that an airport can operate smoothly.
  
  Controllers in MVC are very similar to air traffic controllers. They won't be directly responsible for writing to a database or creating HTML responses, but instead they will direct incoming data to the appropriate models, views, and other packages that can be used to complete the work requested.

  Similar to views, a controller shouldn’t be packed with too much business logic. Instead, they should mostly just parse data and ship it off to other functions, types, etc to handle.

## middleware
  Not everything is a model, view, or controller, middleware is a package to handle HTTP requests that doesn't really fit into the controller package.


