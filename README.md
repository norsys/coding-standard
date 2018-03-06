Coding standard to Norsys PHP projects
======================================

Installation
------------

Edit your `composer.json`

```json
{
    "require-dev": {
        "norsys/php-coding-standard": "~1.0"
    }
}
```

Update your `composer.lock`

```sh
composer update --dev norsys/php-coding-standard
```

Quick usage
-----------

Launch `phpcs` with `Norsys PHP` ruleset

```sh
bin/phpcs --standard=vendor/norsys/php-coding-standard/php
```

Check style specific to write tests
-----------------------------------

```sh
bin/phpcs --standard=vendor/norsys/php-coding-standard/php/test
```

Use with Symfony
----------------

```sh
bin/phpcs --standard=vendor/norsys/php-coding-standard/symfony
bin/phpcs --standard=vendor/norsys/php-coding-standard/symfony/test
```

Advanced usage
--------------

Create your ruleset `my-ruleset.xml`

```xml
<!-- my-ruleset.xml -->

<?xml version="1.0"?>
<ruleset name="MyCustomCheckStyleStandard">

  <description>My custom check style standard based on Norsys</description>

  <!-- Add Norsys rules -->
  <rule ref="vendor/norsys/php-coding-standard/php"/>

  <!-- Your custom rules -->
  ...

</ruleset>
```

Launch `phpcs` with your ruleset

```sh
bin/phpcs --standard=my-ruleset.xml
```

## Credits

Developped by [Norsys](https://www.norsys.fr/)

## License

This project is licensed under the [MIT license](LICENSE).

[![License](https://poser.pugx.org/norsys/php-coding-standard/license)](https://packagist.org/packages/norsys/php-coding-standard)
