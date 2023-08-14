
<!-- documentation   -->
https://symfony.com/doc/current/doctrine.html#installing-doctrine
# Installing Doctrine
composer require symfony/orm-pack
composer require --dev symfony/maker-bundle
# in php.ini we should activate PostgreSQL "/xamp/php/php.ini" -> to enable the drive
enable this feature : 
extension=pdo_pgsql
extension=pgsql
# change the .env variable
DATABASE_URL="postgresql://postgres:bi@localhost:5432/ToDoListTest?serverVersion=15&charset=utf8"
# Finaly you can create your database
php bin/console doctrine:database:create
# create a new table
php bin/console make:entity
# save all tables and migrate into the database
php bin/console make:migration
# execute the migration
php bin/console doctrine:migrations:migrate



<!-- setUp Project -->
composer install
composer update
php bin/console cache:clear

