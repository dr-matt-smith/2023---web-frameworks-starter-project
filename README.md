# CRUD quickstart project

##(1) Change PHPStorm Terminal to the Windows 'cmd' (NOT powershell)

![cmd_terminal_screenshot](_cmd_terminal_screenshot.png)

## (2) Install the certificate so you can run HTTPS: 

```bash
symfony.exe server:ca:install
```


## OLD CRUD quickstart notes .....

To start working with this project you will need to:

- update `.env` with your MySQL credentials
- ensure the `migrations` folder exist, and is EMPTY!
- create the database with `symfony console d:d:c`
- create the SQL table creation (migration) code with `symfony console ma:mi`
- execute the SQL table creation (migration) code with `symfony console d:m:m`
- load the initial data (fixtures) into the DB with  `symfony console d:f:l`

## Run the web server

Run the Symfony web server (in the background) with:
```bash
symfony serve -d
```

## Stop the web server

Stop the Symfony web server with:
```bash
symfony server:stop
```


## Useful - run SQL queries from command line

```bash
symfony console d:q:sql "select * from TABLE"
```

## BONUS - setup for testing (advanced)

If you want to try out some of the tests (in folder `tests`) you'll need to set up the test environment database by doing the follow:

- create the database with `symfony console d:d:c --env=test`
- execute the (existing) SQL table creation (migrations) code with `symfony console d:m:m --env=test`
- load the initial data (fixtures) into the DB with  `symfony console d:f:l --env=test`

## Run the tests

Run the Symfony web server with:
```bash
php bin/phpunit
```


