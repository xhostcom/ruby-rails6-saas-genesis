Ruby Rails 6 SaaS Genesis
================

Ruby project that includes everything you need to create a saas project.

### Getting Set Up

This site runs on **Ruby 2.7.2**, **Rails 6.0.4** and **MySQL**


#### Installing the Site on your Local Machine

1. Make sure to fork this repository
2. When you have it cloned to your local machine make sure your Ruby version is 2.7.2

##### Populating the Database

The `db/seeds.rb` file is used to populate essential information in order to use the system.  Use the command `rake db:seed` to populate the database. You can run it as many times as you'd like, it deletes all meta data and repopulates it with each run.  For now the seed file creates an administrator user but eventually when the curricula get open-sourced like this project it will create a demo site for you to use.

##### Custom configuration files

To avoid conflicts between developers and to store private environment variables like Github API key we use `figaro` gem. `figaro` creates a file called `application.yml` that's located in the `config/` directory but not checked into git (no, you can't have my passwords).

Check out the [Figaro Documentation](https://github.com/laserlemon/figaro) for a very easy-to-understand explanation of how the gem works. You basically just need to run `rails generate figaro:install` and populate the missing variables in `application.yml`.  You can find an example of the requested variables in `config/application.yml.example`.

##### Running the server

Run `rails server` the app should be running at `http://localhost:3000`.

This is basically all you need to get yourself set up with the repository. 

You may have to check your system for mysql libraries see notes in mysqlgemnotes
