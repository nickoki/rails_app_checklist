# Rails App Checklist
A tl;dr checklist to guide your workflow for your new Rails App

### Set Up Rails App

- [ ] `rails new . -d postgresql`

<details>
<summary>_Learn more_</summary>
> Creates a new rails app with a postgresql db (default is sqlite3)
</details>

- [ ] _optionally make changes to_ `/config/database.yml`

- [ ] `rails db:create`

### Models & Migrations

- [ ] `rails g model <name> <attribute:type>`

<details>
<summary>_Learn more_</summary>
> Creates model and migrations, ex. `rails g model Comment body:text post:references`
</details>

- [ ] _optionally make changes to_ `/app/models/<name>.rb`

<details>
<summary>_Learn more_</summary>
> This is where you will update models with relationships, for example
<details>

- [ ] `rails db:migrate`

### Routes & Controllers

- [ ] `rails g controller <name>`

<details>
<summary>_Learn more_</summary>
> Creates a new controller and route (resources)
<details>
