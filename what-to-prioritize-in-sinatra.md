# What to Prioritize in the Sinatra Section

## DO Prioritize:

**ORMs and ActiveRecord Unit: Migrations, CRUD Intro, and Associations**

After this unit you should be able to:
- Understand that migrations are what we write to make changes to our database.
- Explain when the `schema` changes.
- Explain and demonstrate in `tux` how we access objects through ActiveRecord associations defined in our models. (Ex: `current_user.posts` — will return an array of posts that belong to the `current_user` object. Where is the `.posts` method defined?)

**Rack Unit: How the Internet Works, Request/Response Flow, Routes**

Double down on
- Difference between `get`, `post`, `patch`, and `delete` requests and responses.
- How "Dynamic URL Routes" work.
- Practice solidifying your understanding of the Request/Response Flow by drawing your own diagrams of this flow

**MVC and Forms Unit: Model, View, Controller (MVC)**

Get comfortable with why we use this file structure, as MVC will be present in most applications. The MVC structure allows us to separate our application's concern, ultimately optimizing functionality and code organization. A popular analogy that is used is to think about the MVC file structure as a restaurant.

  1. **Model (Database):** Think of the "model" as a the kitchen where the chef is preparing the food, in our case ActiveRecord could be considered the chef and the food is our data.

  2. **View (The Frontend of our Application):** Think of the view as the plate of food that the customer finally sees, this could be considered the "frontend" of our application.

  3. **Controller (Intermediary for the Model and View):** Think of the controller as the waiter goes back and forth between the kitchen and the customer's table. The waiter delivers the plate of food from the kitchen to the customer (end user/frontend) and returns back to the kitchen at the customers request — the plate/customer could be considered the "view" in this analogy.

At the end of this unit you should be able to explain the MVC flow in your own words.

**ActiveRecord Unit: CRUD, Authentication, ActiveRecord Associations**

  - **"Sinatra ActiveRecord CRUD" Lab:** Be sure to get tons of practice with building out Create, Read, Update, and Delete (CRUD) functionality in an application. Not only will CRUD be the basis for the functionality of your Sinatra Final Project, but CRUD is also the base functionality for a lot of the apps we use today like note apps and social media apps like Instagram.

  Be able to answer questions like:

      1. What is the difference between rendering vs. redirecting?
      2. Where do the instance variables in our view files come from — where are they declared and how do we have access to them?


  - **"User Authentication in Sinatra" + "Securing Passwords in Sinatra" Labs:** Double down on these labs to confirm your understanding of the authentication flow in Sinatra. Check for understanding by answering these questions:

      1. What is a `session`? How do I enable it in my application and why?
      2. What are the basics of ActiveRecord's `has_secure_password` method?
      3. What does the `.authenticate` method do and how is it connected to the `has_secure_password` method?
      4. Why do we use the `bcrypt` gem and what is the significance of adding the `password_digest` column to the `User` model in the database?

## DON'T Spend _Too_ Much Time Here:

**SQL (Structured Query Language) Unit**

Let's begin by saying SQL is an important unit. This unit is basically a primer on how we read the queries to our database that will be displayed in our console when our program is running. Being able to read these queries becomes important when we want to do things like debug or collect context clues for an error related to our database. BUT spoiler alert: ActiveRecord will "write" and "read" SQL for us. This unit is dedicated to priming us to the power of database queries and ActiveRecord, so no need to deep dive here _but_ definitely familiarize yourself with SQL queries — being able to read this language comes in handy when investigating the behavior of your database.

**ORMs Sub-Unit**

While ORM is an important concept, at this point it's sufficient to understand it _at a high level_. This sub-unit can get really abstract and it's easy to get lost in the weeds here. Just think of this sub-unit as us laying down the ground work to introduce you to the ActiveRecord magic.

**HTML Continued && CSS Continued Units**

WE KNOW...these units are so fun! This is a _really_ exciting time in the curriculum where we finally spend sometime in the browser. In the CLI section we were in the console for so long that it's really tempting to spend a lot of time here on all the front-end fun. By all means don't skip this section as we are building projects as portfolio pieces and we want them to shine! But at this stage, it would be more wise to invest your time and energy resources in the units above. You can always dive deeper into HTML and CSS later in or after the program.
