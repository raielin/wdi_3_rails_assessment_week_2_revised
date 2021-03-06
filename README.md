# Rails Commands Quiz

Fork, clone, and write your answers directly in this file. Then submit a pull request.

### Question 1 - CORRECT

I want to start a new Rails project/app called `BunnyApp`. What command should I type in the terminal?

  # Create and navigate into new rails directory
    $ rails new BunnyApp --database=postgresql -T
    $ cd BunnyApp

### Question 2 - CORRECT

I want to create a new model called `Bunny`, with the following attributes: name (string), color (string), and age (integer). What command(s) should I type in the terminal and/or Sublime? (In your answer, create both a migration and the model file.)

  $ rails g model Bunny name color age:integer

### Question 3 - CORRECT

What does the command in Question 2 do, exactly? What files are created, where are they located, and what does the database look like at this time? Explain.


  # Rails creates a migration file with the columns and datatypes specified in Ques. 2. Where unspecified, Rails defaults to string type. The associated model files are created as well.

  # I think you'd have to manually create the bunnies_controller.rb controller file, but I'm not totally sure if the model generation will automatically create an empty controller file for you.

  # CORRECTION: Should also mention - no schema and no database created yet

### Question 4 - CORRECT

I want to create a database and make it reflect the new model I created in Question 2. What command(s) should I type in the terminal?

  $ rake db:drop db:create db: migrate


### Question 5 - CORRECT

I want to look at the actual database that has been created. What command should I type in the terminal?

  $ rails db

### Question 6 - CORRECT

I want to see a list of all the URLs available in my app, along with the HTTP requests and controllers associated with them. What command should I type in the terminal?

  $ rake routes

### Question 7 - CORRECT

What line should I add to `config/routes.rb` to create a complete set of RESTful routes for a "bunnies" resource?

  resources bunnies

### Question 8 - CORRECT

According to standard Rails conventions, what directory and filename would the BunniesController be located in, starting from the root of the project?

  BunnyApp/app/controllers

### Question 9 - CORRECT

According to standard Rails conventions, what directory and filename would the "show" view for bunnies be located in, starting from the root of the project?

  BunnyApp/app/views/bunnies/show.html.erb

### Question 10 - CORRECT

I have worked on my app and finally want to see it in action. What command should I type in the terminal, and where should I navigate to in my browser?

  $ rails server

  Navigate to the local host port, in our case: localhost:3000/bunnies

  (unless you specified the root to direct to bunnies#index in config/routes.rb, in which case, you can just browse to localhost:3000)
