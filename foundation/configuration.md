# Configuration

- [Sample Configuration](#sample-configuration)
- [Reference](#reference)
- [Authentication](#authentication)
- [Dashboard](#dashboard)

This page provides a quick overview of all of the options provided in ```anavel.php```, the base configuration file for Anavel.

### <a name="sample-configuration"></a> Sample Configuration

```php
<?php

return [
    /*
    |--------------------------------------------------------------------------
    | Route prefix
    |--------------------------------------------------------------------------
    |
    */
    'route_prefix' => 'admin',

    /*
    |--------------------------------------------------------------------------
    | Site name
    |--------------------------------------------------------------------------
    |
    */
    'site_name' => 'Anavel',

    /*
    |--------------------------------------------------------------------------
    | Skin
    |--------------------------------------------------------------------------
    | skin-blue, skin-yellow, skin-purple, skin-green, skin-red, skin-black
    */
    'skin' => 'skin-black',

    /*
    |--------------------------------------------------------------------------
    | Skin
    |--------------------------------------------------------------------------
    | fixed, layout-boxed, sidebar-collapse
    */
    'layout_options' => '',

    /*
    |--------------------------------------------------------------------------
    | Authentication Driver
    |--------------------------------------------------------------------------
    | laravel
    */
    'auth_driver' => 'laravel',

    /*
    |--------------------------------------------------------------------------
    | Languages used for translated models
    |--------------------------------------------------------------------------
    |
    */
    'translation_languages' => [

    ],

    /*
    |--------------------------------------------------------------------------
    | CKeditor uploads path
    |--------------------------------------------------------------------------
    |
    */
    'ckeditor_uploads_path' => 'uploads/ckeditor',

    /*
    |--------------------------------------------------------------------------
    | Modules
    |--------------------------------------------------------------------------
    |
    */
    'modules' => [

    ],

    /*
    |--------------------------------------------------------------------------
    | Dashboard view
    |--------------------------------------------------------------------------
    |
    */
    'dashboard_view' => 'anavel::pages.index',
];
```

### <a name="reference"></a> Reference

| Property | Explanation | Notes |
|:-----------|------------|------------|
| **route_prefix** | The prefix to access to any Anavel route | |
| **site_name** | The admin panel displayed name | You can use html tags and images |
| **skin** | The skin color to use base the admin panel | Available: skin-blue, skin-yellow, skin-purple, skin-green, skin-red, skin-black |
| **layout_options** | The different layout options to apply | Available: fixed, layout-boxed, sidebar-collapse |
| **auth_driver** | The driver to use for user authentication | Currently only implemented with the built in Laravel. Check the [authentication](#authentication) section |
| **translation_languages** | The site available languages | |
| **ckeditor_uploads_path** | The ckeditor file uploads path | |
| **modules** | The configured modules for the admin panel | |
| **dashboard_view** | The first view that your users will see when they access the admin panel | Check the [dashboard](#dashboard) section to see how to customize it |

### <a name="authentication"></a> Authentication

The Anavel authentication integrates with the built in Laravel authentication, check the [official documentation](https://laravel.com/docs/authentication). 

The only Anavel particular thing that you must to do is implement the ```Anavel\Foundation\Contracts\Authenticatable``` interface with your ```User``` model.

### <a name="dashboard"></a> Dashboard

If you want to customize your dashboard view you can do it by configuring your custom view as ```dashboard_view``` in the ```anavel.php``` config file. For display the view data we recomend use a [View Composer](https://laravel.com/docs/views#view-composers). 
