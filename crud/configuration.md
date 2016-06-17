# Configuration

- [Sample Configuration](#sample-configuration)
- [Reference](#reference)
- [Model](#model)
- [Menu](#menu)

This page provides a quick overview of all of the options provided in `anavel-crud.php`, the configuration file for Anavel.

### <a name="sample-configuration"></a> Sample Configuration

```php
<?php

return [
    /*
    |--------------------------------------------------------------------------
    | Displayed name
    |--------------------------------------------------------------------------
    |
    */
    'name' => 'CRUD',

    /*
    |--------------------------------------------------------------------------
    | Displayed icon
    |--------------------------------------------------------------------------
    |
    */
    'icon' => 'fa-database',

    /*
    |--------------------------------------------------------------------------
    | Paginate lists by
    |--------------------------------------------------------------------------
    |
    */
    'list_max_results' => 15,

    /*
    |--------------------------------------------------------------------------
    | File uploads path
    |--------------------------------------------------------------------------
    |
    */
    'uploads_path' => '/storage/resources/',

    /*
    |--------------------------------------------------------------------------
    | Text Editor
    |--------------------------------------------------------------------------
    | ckeditor, bootstrap-wysihtml5
    */
    'text_editor' => 'ckeditor',

    /*
    |--------------------------------------------------------------------------
    | Configured models
    |--------------------------------------------------------------------------
    |
    */
    'models' => [],
    
    /*
    |--------------------------------------------------------------------------
    | Menu agrupations
    |--------------------------------------------------------------------------
    |
    */
    'modelsGroups' => []

];

```

### <a name="reference"></a> Reference

| Property | Explanation | Notes |
|:-----------|------------|------------|
| **name** | The name to display in the admin panel for the module | |
| **icon** | The icon to display in the admin panel for the module | |
| **list_max_results** | By default listings display a maximum of 15 rows, but you can customize it with this config key | |
| **uploads_path** | The folder (under public) on which your resources files will be uploaded | |
| **text_editor** | The WYSIWYG to use | |
| **models** | This contains all the Eloquent models configuration that will be managed by this module | Check the [model](#model) section to see more details |
| **modelsGroups** | With this key you can group model CRUD access on the admin | Check the [menu](#menu) section to see more details |

### <a name="model"></a> Model

To start "cruding" your models just add them to the config file as follows:

```php
# ...
'models' => [
    'Users'      => App\User::class,
    'Blog Posts' => App\Post::class
# ...
```

This is all that you need to do to get a full-featured CRUD on your admin panel. But most of times the default behaviour isn't enough, so keep reading to see all the config options to get your custom crud.

#### Relations

```php
# ...
'models' => [
    'Blog Posts' => [
        'model' => App\Post::class,
        'relations' => [
            'author' => [
                'name' => 'author',
                'display' => 'name'
            ]
        ]
    ]
# ...
```

#### List customization

```php
# ...
'models' => [
    'Blog Posts' => [
        'model' => App\Post::class,
        'list' => [
            'display' => ['id', 'translations.title', 'is_public', 'created_at', 'updated_at']
        ]
    ]
# ...
```

#### Create/Edit customization

### <a name="menu"></a> Menu
