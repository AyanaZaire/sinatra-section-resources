# Sinatra Project Order of Operations Guide

The Sinatra Project repo has a helpful [`spec.md` file](https://github.com/learn-co-students/sinatra-cms-app-assessment-online-web-sp-000/blob/master/spec.md) that outlines the requirements for the Sinatra Project but we wanted to outline a suggested flow of execution. We put together this "Order of Operations Guide" for organizing and completing your Sinatra Project. This guide is based on the 4-part project build that happens ever 2-week study group cycle. All study groups can be found [here](https://learn.co/study-groups).

The application we build in the project build is an "Artist Portfolio App". **User story: A user should be able to login/sign up to post, edit, or delete their artwork or see the artwork of other users.**

## Checklist

### PART 1 — Project Setup: Corneal, MVC, ActiveRecord

**BEFORE YOU CODE**
- [ ] 1. Check project requirements in `spec.md`
- [ ] 2. Ideate! What do you want to build?
  - choose a domain you're familiar with!
  - choose a domain you care about
- [ ] 3. Wireframing & User Stories
  - Write down your models, their attributes, and their associations
  - "As a user, I can ....."
  - "A user should be able to ....."
  - What does your app _do_?
- [ ] 4. Design your MVP = 'Minimum Viable Product' vs. what are my 'stretch goals'
  - Stretch goals - bonus features you want but don't need

**NOW WE CODE (BUT JUST OUR MODELS — NO CONTROLLERS OR VIEWS)**

- [ ] 5. Generate new project using [corneal gem](https://github.com/thebrianemory/corneal)
- [ ] 6. Create github repo
- [ ] 7. Build your models
  - Migrations
  - Model classes
  - Associations
- [ ] 8. Test your models and associations in the console
  - Create some seed data
  - Adjust migrations as needed

### PART 2 — User Authentication: Login + Sign Up

**NOW, CONSIDER USER CONTROLLER, APPLICATION CONTROLLER, AND VIEWS**

*IMPORTANT:* Build views and controller actions based on the flow of your app, one step at a time, testing as you go!

- Use `shotgun` and `pry` (or `raise`/`inspect`) all the time!

**START WITH LOGIN**

- [ ] 9. Create your `UsersController`
  - Mount new controller in `config.ru` with `use UsersController` (Why do we add this?)

- [ ] 10. Enable `sessions` in `ApplicationController`
    - Enable sessions
    - Create session secret

- [ ] 11. Build routes and views for login
  - Build your `get` login route + "login" view
  - Build your `post` login route
      - **Tip**: Here is where we authenticate the user and leverage the session hash to log them in!
  - Build your `get users/:id` route + "show" view

- [ ] 12. Create your `ApplicationController` helper methods
  - **Ask**: Why do we add this?
  - `#logged_in?`: checks if the user is logged in
  - `#current_user`: keeps track of the user currently logged in

**MOVE ON TO SIGN UP**
- [ ] 13. Build routes and views for signup
  - Build your `get` signup route + "signup" view
  - Build your `post` signup route

**WRAP UP WITH LOG OUT**
- [ ] 14. Build your `get` logout route

### PART 3 — CRUD: Create, Read, Update, Delete

- [ ] 15. Create your `PostsController`
  - Mount new controller in `config.ru` with `use PostsController`
  - **Ask**: Why do we add this? ^

- [ ] 16. Implement READ functionality
  - Create `get` posts route
  - Create a view for displaying all posts

- [ ] 17. Implement CREATE functionality
  - Create `get` posts route and view to render form
  - Create `post` route to create new post

- [ ] 18. Implement UPDATE functionality
  - Add `use Rack::MethodOverride` in `config.ru`
  - **Ask**: Why do we add this? ^
  - Create `get` route and view to render form
  - Create `patch` route to update an existing post

- [ ] 19. Implement DELETE functionality
  - Create `delete` form in relevant view
  - Create `delete` route to delete post

### PART 4 — Tighten Up!: Validations and Authorization
- [ ] 20. Implement `sinatra-flash` gem to display validation failures and improve user experience (UX)
  - Review the [docs](https://github.com/SFEley/sinatra-flash)
  - **Tip**: a `flash[:message]` has the lifecyle of one `GET` request and will not show up when rendering an `erb` file.
- [ ] 21. Include ActiveRecord validations in your `User` and `Post` model that checks for user inputs
  - **Ex**: Making sure all form fields are filled out or that a user is using a unique email or username
  - Review the [docs](https://guides.rubyonrails.org/active_record_validations.html)
  - **Tip**: `has_secure_password` has a built in validation for the `password_digest` attribute!
- [ ] 22. Leverage the `logged_in?` helper method in the controller and/or views to implement authorization for creating a new post.
  - Make sure a user can't create a new post without being logged in.
- [ ] 23. Implement authorization to edit and delete.
  - Make sure a user can't edit or delete a post that doesn't belong to them.
- [ ] 24. Refactor your code to make it more DRY!
  - **Ask**: Where am I repeating myself?
- [ ] 25. Create a `README.md`
  - Include a short description, install instructions, a contributors guide and a link to the license for your code

### Bonus
- [ ] Leverage a CSS framework to improve the styling of your application
  - Easiest to implement: [Bulma](https://bulma.io/)
  - Most popular: [Bootstrap](https://getbootstrap.com/)
  - Also good: [Semantic UI](https://semantic-ui.com/)
  - Not bootstrap: [Materialize](https://materializecss.com/)

### Confirm
- [ ] You have a large number of small Git commits
- [ ] Your commit messages are meaningful
- [ ] You made the changes in a commit that relate to the commit message
- [ ] You don't include changes in a commit that aren't related to the commit message
