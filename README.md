# Rails App Checklist
A tl;dr checklist to guide your workflow for your new Rails App

### Set Up Rails App & Database

- `rails new . -d postgresql`
  - creates a new rails app with a postgresql db (default is sqlite3)
  - this also runs `bundle install`
  
- _optionally add (or remove) gems to_ `Gemfile` and run `bundle install` afterwards

- _optionally make changes to_ `/config/database.yml`
  - if changes are made here after init, run `rails db:drop`

- `rails db:create`

### Models & Migrations

- create your ERD

- `rails g model <model_name> <attribute:type> ...`
  - creates migration and model, ex. `rails g model Comment body:text post:references`
  - _note: be sure to only_ `reference` _models that already exist_
    - to add a reference later, use `rails g migration <migration_name> <reference_name>:references`
    - ex. `rails g migration AddHouseRefToCharacters house:references`

- _optionally make changes to_ `/app/models/<name>.rb`
  - this is where you will update models with relationships, for example

- `rails db:migrate`

### Seeds

- _optionally create seed data in_ `/db/seeds.rb`

- `rails db:seed`

### Routes, Controllers, and Views

- `rails g controller <controller_name (plural)>`
  - creates a new controller file and views folder
  
- update `config/routes.rb`
  - `resources :<controller_name (plural)>`
  
- begin work on you controller and views

-----

### Helpful Ruby Snippets

- `root to: "<controller>#<action>"`

