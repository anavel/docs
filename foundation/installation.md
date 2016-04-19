# Installation

To start using Anavel you must install the foundation package, which is the admin panel backbone and over which are installed the modules (the real useful pieces of Anavel) with the different functionalities. So, let's start by requiring this package with composer:

```
composer require anavel/foundation
```

After updating composer, add the ServiceProvider to the app.php config file:

```php
// config/app.php

'providers' => [
    '...',
    Anavel\Foundation\AnavelServiceProvider::class,
];
```

Copy the package config and assets to your project folders with the publish command:

```
php artisan vendor:publish
```
