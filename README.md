# E-Commerce-Backend
 
 ## Table of contents
* [General info](#general-info)
* [How to use](#how-to-use)


## General Info
Here we are building a backend using express and creating a database with mysql for an ecommerce app. 

We use the `schema.sql` file in the `db` folder to create your database with MySQL shell commands. We use environment variables to store sensitive data like your MySQL username, password, and database name.

our database should contain the following four models, including the requirements listed for each model:

* `Category`

  * `id`

    * Integer.
  
    * Doesn't allow null values.
  
    * Set as primary key.
  
    * Uses auto increment.

  * `category_name`
  
    * String.
  
    * Doesn't allow null values.

* `Product`

  * `id`
  
    * Integer.
  
    * Doesn't allow null values.
  
    * Set as primary key.
  
    * Uses auto increment.

  * `product_name`
  
    * String.
  
    * Doesn't allow null values.

  * `price`
  
    * Decimal.
  
    * Doesn't allow null values.
  
    * Validates that the value is a decimal.

  * `stock`
  
    * Integer.
  
    * Doesn't allow null values.
  
    * Set a default value of `10`.
  
    * Validates that the value is numeric.

  * `category_id`
  
    * Integer.
  
    * References the `Category` model's `id`.

* `Tag`

  * `id`
  
    * Integer.
  
    * Doesn't allow null values.
  
    * Set as primary key.
  
    * Uses auto increment.

  * `tag_name`
  
    * String.

* `ProductTag`

  * `id`

    * Integer.

    * Doesn't allow null values.

    * Set as primary key.

    * Uses auto increment.

  * `product_id`

    * Integer.

    * References the `Product` model's `id`.

  * `tag_id`

    * Integer.

    * References the `Tag` model's `id`.


We need to execute association methods on your Sequelize models to create the following relationships between them:

* `Product` belongs to `Category`, and `Category` has many `Product` models, as a category can have multiple products but a product can only belong to one category.

* `Product` belongs to many `Tag` models, and `Tag` belongs to many `Product` models. Allow products to have multiple tags and tags to have many products by using the `ProductTag` through model.



## How to Use

In the video below shows how to run th app from the terminal.

*navigate to the root folder of the app then run npmi to istall dependencies
*enter mysql -u root -p to start up mysql
*enter source schema.sql to create the database
*enter quit to exit mysql
*run npm run seed to seed the database
*run npm start to run the app

We can then check our api routes using Postman
 
 First walkthrough video

https://user-images.githubusercontent.com/39675578/181937716-e6854f51-688d-4412-a453-7877ae0bcf52.mp4

second walkthrough video

Checking the api routes




https://user-images.githubusercontent.com/39675578/181978173-afe004c4-001f-4004-afa6-9be538a44e31.mp4

