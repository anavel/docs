# Instalation

With Anavel Foundation installed and working, require this package with composer:

```
composer require anavel/crud
```

After updating composer, add the ModuleProvider to the modules array in ```anavel.php``` config file:

```
Anavel\Crud\CrudModuleProvider::class
```

Copy the package config to your local config with the publish command:

```
php artisan vendor:publish
```
