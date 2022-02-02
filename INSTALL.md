# Installation Instructions

- Create a local database for the project
- Run `cp .env.example .env` command to copy example into real .env file, then edit it with DB credentials and other settings you want.
- Run `composer install` command
- Run `php artisan migrate --seed` command. Seed is important, because it will create the first admin user for you.
- Run `php artisan key:generate` command
- If you have file/photo upload fields, run `php artisan storage:link` command
- And that's it, go to your domain (or use `php artisan serve`) and login with these credentials: `admin@admin.com - password`
