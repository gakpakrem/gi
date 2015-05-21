## Dick - The Admin Panel Builder for Laravel


Dick helps you kickstart your Laravel project, providing baseline code and interface for what any/many projects will need:
- CRUD interface (inspired by Grocery Crud for CodeIgniter);
- Authentication, user, role and permission management (using Laravel Auth & Entrust);
- Superadmin tools:
    + file & database backup;
    + log file viewer;
    + file manager;



Version: 0.5 (alpha)

Website: http://usedick.com

Documentation: http://usedick.com/docs



It's heavily opinionated and uses:
- Laravel 5
- Bootstrap 3
- jQuery
- AdminLTE theme


------------

### Installation
(for alpha version)


1. Like any Laravel 5 installation, run:

    chmod -R o+w storage
    chmod -R o+w vendor

2. Run the migration to get the users table:

    php artisan migrate

3. Create a user for yourself at:
http://localhost/dick/public/auth/register


------------

### How to create a new CRUD Panel for an entity

1. Generate a new resource controller in the command line:
php artisan make:controller ArticleController

2. Modify the new controller to extend CrudController and delete or comment any methods you don't need.

3. Create a model for your entity.
php artisan make:model Models/Article

4. Create a route for it in routes.php:
Route::resource('article', 'ArticleController');

See detailed installation&use of the CRUD panel here: http://usedick.com/docs