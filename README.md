# Multiple Relationships in Rails

## Objectives
1. Practice Active Record relationships
2. Create Migrationos, Models, and Controllers
3. Create connections through Models beyond join tables
4. Apply understanding of Active Record relationships

## Instructions
Welcome to the life of a parent. If your kid has something, that means it is yours too. Your goal is to make a M:N Parent to Kid relationship -because a kid can have many parents, biological and otherwise. After that, make a 1:M relationhip between a kid and their toys. Finally, make a M:N relationship between a kid and the sports they play. By the end you should be able to call `parent.toys` and `parent.sports` to know what responsibilities you signed up for, through your kid.

Fork and clone to get started. Run `bundle`. Code away!

### Part 1:  Create the relationship between Parent and Kid
This is a M:N. Make the migrations, models, route, and controller. Seed at least 3 parents and 3 kids, then connect them. Make a `GET` request to `/parents` to see each parent and their kids. Use `rails c` or `rails console` to test your relationships before completing your controller.

### Part 2: Create the relationship between Kid and Toy
This is a 1:M. Make the migration, model, and controller. Seed at least 3 toys. Make a `GET` request to `/parents` to see each parent, their kids, and the 'parents' toys. Use `rails c` to test your relationships -you should be able to run `kid.toys` and `parent.toys`.

### Part 3: Create the relationship between Kid and Sport
This is a M:N. Make the migrations, models, and controller. Seed at least 3 sports, then connect them to kids. Make a `GET` request to `/parents/` to see each parent, their kids, the 'parents' toys, and the 'parents' sports. User `rails c` to test your relationships -you should be able to run `kid.sports` and `parent.sports`.

# Tips
* Going `through` a model to make a relationship can be used for more than pure join tables.
* `rails c` or `rails console` is your best friend for testing relationships before moving past your migrations and seeds.
* You'll need to use `include` in your controller.

## Bonus
All the following will require more code:
* Use Postman to create a new Toy.
* Use Postman to create a new Kid and Toy in the same request. (This will require accepting nested attributes).
* Use Postman to connect a kid to an existing sport they are NOT already connected to.