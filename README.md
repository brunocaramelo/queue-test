RUN BEFORE THE CLIENT APPLICATION

1- Create the Database (Mysql) run DUMP of storage/database/create-database.sql

2 - Change parameters in .env for the Database DB_CONNECTION=mysql DB_HOST=127.0.0.1 DB_PORT=3306 DB_DATABASE=stock_api DB_USERNAME=root DB_PASSWORD=testes

3 - RUN migrations and seeds - run in the root - php artisan migrate - php artisan db:seed if you want to use the API

4 - Test battery using sqlite with the phpunit command in the project root
    - API Tests
    - Unit Tests

Routes:

    GET - v1/products/ (List Products)

    GET - v1/products/{id} (Detail Products)

    PUT - v1/products/{id} (Edit Products)
    POST - v1/upload/ (Import Products, Send spreadsheet in the [file] field)
    DELETE - v1/products/{id} (Delete Products)
    GET - v1/upload/check-proccess (List Processes)
    GET - v1/products/check-proccess/{id} (Detail Process)

JOB DRIVER used: database

execute

    php artisan migrate ;
    php artisan db:seed ;
    php artisan queue:listen
  