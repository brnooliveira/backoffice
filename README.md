# README

# Steps:

    1. rails generate controller welcome index and set routes root 
    2. add: gem "devise"
    3. rails generate devise:install
    4. config devise in config/environments/development.rb
    5. rails generate devise Admin
    6. rails generate devise User
    7. config config/initializes/devise.rb : config.scoped_views = true for two views elements
    8. rails generate devise:views admins
    9. rails generate devise:views users
    10. rails db:migrate

    --- backoffice ---

    1. rails generate controller admins_backoffice/welcome index
    2. rails generate controller users_backoffice/welcome index
    3. rails generate controller users_backoffice and assign to users_backoffice/welcome_controller.rb
    4. rails generate controller admins_backoffice and assign to admins_backoffice/welcome_controller.rb
    5. protecting backoffice:
        . before_action :authenticate_admin! to protect admins in admins_backoffice_controller.rb
        . before_action :authenticate_users! to protect profile users_backoffice_controller.rb
    
    -------------------

    11. CONFIG LOGOUT! in views admins_backoffice/welcome and users_backoffice/welcome
  


