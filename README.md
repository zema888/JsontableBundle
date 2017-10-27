JsontableBundle
===============

Form type for display of array type data in the form of a table.

Installation
------------

1. Add this bundle to your project in composer.json:

	```
    {
        "require": {
            "zema888/jsontable-bundle": "dev-master",
        }
    }
    ```
    
2. Run the composter to download the bundle:

    php composer.phar update zema888/jsontable-bundle
    
3. Register this bundle to your app/AppKernel.php:

    ```
    // app/AppKernel.php
    public function registerBundles()
    {
        return array(
            // ...
            new Zema888\JsontableBundle\JsontableBundle(),
            // ...
        );
    }
    
#Usage#

Use widget in your forms (works with SonataAdmin too) to create a simple image field:

->add('arr1', 'jsontable', [
        'label' => 'Name field',
        "required" => false,
        "keys" => ['title','text'],
        "labeles" => [ 'Name', 'description'],
        "fixed_row" => true
    ])