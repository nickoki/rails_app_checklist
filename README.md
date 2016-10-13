# Rails App Checklist
A tl;dr checklist to guide your workflow for your new Rails App

### Set Up Rails App & Database

- `rails new . -d postgresql`
  - creates a new rails app with a postgresql db (default is sqlite3)
  - this also runs `bundle install`
  
- _optionally add new gems to_ `Gemfile` and run `bundle install` afterwards

- _optionally make changes to_ `/config/database.yml`

- `rails db:create`

### Models & Migrations

- `rails g model <name> <attribute:type> ...`
  - creates migration and model, ex. `rails g model Comment body:text post:references`
  - note: be sure to only `reference` models that already exist

- _optionally make changes to_ `/app/models/<name>.rb`
  - this is where you will update models with relationships, for example

- `rails db:migrate`

### Seeds

- _optionally create seed data in_ `/db/seeds.rb`

- `rails db:seed`

### Routes, Controllers, and Views

- `rails g controller <name>`
  - creates a new controller and routes (resources)
  
- begin work on you controller and views

-----

### Helpful Ruby Snippets

- ``

