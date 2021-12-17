Run a migration to create table

To create a migration, you may use the make:migration command on the Artisan CLI (artisan command line interface):

php artisan make:migration create_users_table
or

php artisan make:migration create_users_table --create=users
Run a migration to alter table

When you need to do some changes in database table example: add field vote to user table you can do like this in your Laravel code without touching SQL code

php artisan make:migration add_votes_to_users_table --table=users
Rollback the last migration operation

If you make mistake and did something wrong you can always rollback to return database in previous state.

php artisan migrate:rollback --step=1
https://stackoverflow.com/questions/30287896/rollback-one-specific-migration-in-laravel

php artisan migrate:rollback
Rollback all migrations

php artisan migrate:reset
Rollback all migrations and run them all again

php artisan migrate:refresh

php artisan migrate:refresh --seed

https://stackoverflow.com/questions/30220377/how-do-laravel-migrations-work

php artisan migrate:refresh --path=/database/migrations/my_migration.php

https://stackoverflow.com/questions/47151886/how-can-i-run-specific-migration-in-laravel

https://stackoverflow.com/questions/16791613/add-a-new-column-to-existing-table-in-a-migration

