Opis Closure
====================
[![Build Status](https://travis-ci.org/opis/closure.svg?branch=4.x)](https://travis-ci.org/opis/closure)
[![Latest Stable Version](https://poser.pugx.org/opis/closure/v/stable.png)](https://packagist.org/packages/opis/closure)
[![Latest Unstable Version](https://poser.pugx.org/opis/closure/v/unstable.png)](https://packagist.org/packages/opis/closure)
[![License](https://poser.pugx.org/opis/closure/license.png)](https://packagist.org/packages/opis/closure)

Serializable closures
---------------------
> Opis Closure 4.x is still in development and we do not recommend using it in production yet.

**Opis Closure** is a PHP library that makes all closures serializable. 
All you have to do is to add a single line of code, and you are good to go.

```php
\Opis\Closure\init();
```

If you are using this library on a server environment and you have preload enabled (which you should), then 
pass `true` as an argument to the `init` function. 

```php
# preload.php
\Opis\Closure\init(true);
```

This version of **Opis Closure** is a full rebuild of the library and is not compatible with the previous versions.
The library use [FFI] to make closures serializable and you no longer need to wrap them as it was the case in the past.

We would like to release a stable version as soon as possible, 
so please test it rigorously and report any errors you have encountered. Feedback is welcome.

### License

**Opis Closure** is licensed under the [MIT License (MIT)][license].

### Requirements

* PHP ^7.4
* FFI

## Installation

**Opis Closure** is available on [Packagist] and it can be installed from a 
command line interface by using [Composer]. 

```bash
composer require opis/closure:4.x-dev
```

Or you could directly reference it into your `composer.json` file as a dependency

```json
{
    "require": {
        "opis/closure": "4.x-dev"
    }
}
```


[documentation]: https://www.opis.io/closure "Opis Closure"
[license]: http://opensource.org/licenses/MIT "MIT License"
[Packagist]: https://packagist.org/packages/opis/closure "Packagist"
[Composer]: https://getcomposer.org "Composer"
[CHANGELOG]: https://github.com/opis/closure/blob/master/CHANGELOG.md "Changelog"
[FFI]: https://www.php.net/manual/en/book.ffi.php "Foreign Function Interface"