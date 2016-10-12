# Rails App Checklist
A tl;dr checklist to guide your workflow for your new Rails App

### Set Up Rails App

- `rails new . -d postgresql`
  - Creates a new rails app with a postgresql db (default is sqlite3)

- _optionally make changes to_ `/config/database.yml`
  - `rails db:create`

### Models & Migrations

- `rails g model <name> <attribute:type>`
  - Creates model and migrations, ex. `rails g model Comment body:text post:references`

- _optionally make changes to_ `/app/models/<name>.rb`
  - This is where you will update models with relationships, for example

- `rails db:migrate`

### Routes & Controllers

- `rails g controller <name>`
  - Creates a new controller and route (resources)

