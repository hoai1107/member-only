# README

Project description link: [Project Description](https://www.theodinproject.com/lessons/ruby-on-rails-members-only)

Summary: Build blog app where any user can view posts but only logged in users can create posts view author.

- Learn how to install and init Devise in a Rails app.
  - Add `devise` to Gemfile
  - Run `rails g devise:install` to init Devise in Rails app
  - Run `rails g devise <model-name>` to generate a devise model for user. Ex. rails g devise user will generate a model User in the app.
- Use Devise filter and helper to manage authentication
  - Use `before_action :authenticate_user!` to restrict access to certain controller actions
    ```ruby
      before_action :authenticate_user!, only: %i[new create]
    ```
  - Use `current_user` to access the current user object