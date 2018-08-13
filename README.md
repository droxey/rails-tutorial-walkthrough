# Ruby/Rails Walkthrough

## Learning Objectives

### Chapter 1: From Zero to Deploy

* Ruby on Rails is a web development framework written in the Ruby programming language.

* Installing Rails, generating an application, and editing the resulting files is easy using a pre-configured cloud environment.

* Rails comes with a command-line command called rails that can generate new applications (`rails new`) and run local servers (`rails server`).

* We added a controller action and modified the root route to create a “hello, world” application.

* We protected against data loss while enabling collaboration by placing our application source code under version control with Git and pushing the resulting code to a private repository at Bitbucket.

* We deployed our application to a production environment using Heroku.

### Chapter 2: A Toy App

* Scaffolding automatically creates code to model data and interact with it through the web.

* Scaffolding is good for getting started quickly but is bad for understanding.

* Rails uses the Model-View-Controller (MVC) pattern for structuring web applications.

* As interpreted by Rails, the REST architecture includes a standard set of URLs and controller actions for interacting with data models.

* Rails supports data validations to place constraints on the values of data model attributes.

* Rails comes with built-in functions for defining associations between different data models.

* We can interact with Rails applications at the command line using the Rails console.

### Chapter 3: Mostly Static Pages

* For a third time, we went through the full procedure of creating a new Rails application from scratch, installing the necessary gems, pushing it up to a remote repository, and deploying it to production.

* The rails script generates a new controller with `rails generate controller ControllerName <optional action names>`.

* New routes are defined in the file `config/routes.rb`.

* Rails views can contain static HTML or embedded Ruby (ERb).

* Automated testing allows us to write test suites that drive the development of new features, allow for confident refactoring, and catch regressions.

* Test-driven development uses a “Red, Green, Refactor” cycle.

* Rails layouts allow the use of a common template for pages in our application, thereby eliminating duplication.

### Chapter 4: Rails Flavored Ruby

* Ruby has a large number of methods for manipulating strings of characters.

* Everything in Ruby is an object.

* Ruby supports method definition via the def keyword.

* Ruby supports class definition via the class keyword.

* Rails views can contain static HTML or embedded Ruby (ERb).

* Built-in Ruby data structures include arrays, ranges, and hashes.

* Ruby blocks are a flexible construct that (among other things) allow natural iteration over enumerable data structures.

* Symbols are labels, like strings without any additional structure.

* Ruby supports object inheritance.

* It is possible to open up and modify built-in Ruby classes.

* The word “deified” is a palindrome.

### Chapter 5: Filling in the Layout

* Using HTML5, we can define a site layout with logo, header, footer, and main body content.

* Rails partials are used to place markup in a separate file for convenience.

* CSS allows us to style the site layout based on CSS classes and ids.

* The Bootstrap framework makes it easy to make a nicely designed site quickly.

* Sass and the asset pipeline allow us to eliminate duplication in our CSS while packaging up the results efficiently for production.

* Rails allows us to define custom routing rules, thereby providing named routes.

* Integration tests effectively simulate a browser clicking from page to page.

### Chapter 6: Modeling Users

* Migrations allow us to modify our application’s data model.

* Active Record comes with a large number of methods for creating and manipulating data models.

* Active Record validations allow us to place constraints on the data in our models.

* Common validations include presence, length, and format.

* Regular expressions are cryptic but powerful.

* Defining a database index improves lookup efficiency while allowing enforcement of uniqueness at the database level.

* We can add a secure password to a model using the built-in `has_secure_password` method.

### Chapter 7: Sign Up

* Rails displays useful debug information via the debug method.

* Sass mixins allow a group of CSS rules to be bundled and reused in multiple places.

* Rails comes with three standard environments: development, test, and production.

* We can interact with users as a resource through a standard set of REST URLs.

* Gravatars provide a convenient way of displaying images to represent users.

* The `form_for` helper is used to generate forms for interacting with Active Record objects.

* Signup failure renders the new user page and displays error messages automatically determined by Active Record.

* Rails provides the flash as a standard way to display temporary messages.

* Signup success creates a user in the database and redirects to the user show page, and displays a welcome message.

* We can use integration tests to verify form submission behavior and catch regressions.

* We can configure our production application to use SSL for secure communications and Puma for high performance.

### Chapter 8: Log In

* Rails can maintain state from one page to the next using temporary cookies via the session method.

* The login form is designed to create a new session to log a user in.

* The flash.now method is used for flash messages on rendered pages.

* Test-driven development is useful when debugging by reproducing the bug in a test.

* Using the session method, we can securely place a user id on the browser to create a temporary session.

* We can change features such as links on the layouts based on login status.

* Integration tests can verify correct routes, database updates, and proper changes to the layout.

### Chapter 9: Advanced Login

* Rails can maintain state from one page to the next using persistent cookies via the cookies method.

* We associate to each user a remember token and a corresponding remember digest for use in persistent sessions.

* Using the cookies method, we create a persistent session by placing a permanent remember token cookie on the browser.

* Login status is determined by the presence of a current user based on the temporary session’s user id or the permanent session’s unique remember token.

* The application signs users out by deleting the session’s user id and removing the permanent cookie from the browser.

* The ternary operator is a compact way to write simple if-then statements.

### Chapter 10: Updating, Showing, and Deleting users

* Users can be updated using an edit form, which sends a PATCH request to the update action.

* Safe updating through the web is enforced using strong parameters.

* Before filters give a standard way to run methods before particular controller actions.

* We implement an authorization using before filters.

* Authorization tests use both low-level commands to submit particular HTTP requests directly to controller actions and high-level integration tests.

* Friendly forwarding redirects users where they wanted to go after logging in.

* The users index page shows all users, one page at a time.

* Rails uses the standard file `db/seeds.rb` to seed the database with sample data using `rails db:seed`.

* Running `render @users` automatically calls the `_user.html.er`b partial on each user in the collection.

* A boolean attribute called admin on the User model automatically creates an admin? boolean method on user objects.

* Admins can delete users through the web by clicking on delete links that issue DELETE requests to the Users controller destroy action.

* We can create a large number of test users using embedded Ruby inside fixtures.

### Chapter 11/12: Account Activation / Password Reset

* Like sessions, account activations can be modeled as a resource despite not being Active Record objects.

* Rails can generate Action Mailer actions and views to send email.

* Action Mailer supports both plain-text and HTML mail.

* As with ordinary actions and views, instance variables defined in mailer actions are available in mailer views.

* Account activations use a generated token to create a unique URL for activating users.

* Account activations use a hashed activation digest to securely identify valid activation requests.

* Both mailer tests and integration tests are useful for verifying the behavior of the User mailer.

* We can send email in production using SendGrid.
