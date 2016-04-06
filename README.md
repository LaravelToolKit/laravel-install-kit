# Laravel Install Kit

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Software License][ico-license]](LICENSE.md)
[![Build Status][ico-travis]][link-travis]
[![Total Downloads][ico-downloads]][link-downloads]

**Note:** Replace ```shawn sandy``` ```shawnsandy``` ```shawnsandy.com``` ```shawnsandy04@gmail.com``` ```shawnsandy``` ```laravel-install-kit``` ```Simple desctriptiption``` with their correct values in [README.md](README.md), [CHANGELOG.md](CHANGELOG.md), [CONTRIBUTING.md](CONTRIBUTING.md), [LICENSE.md](LICENSE.md) and [composer.json](composer.json) files, then delete this line.

This is where your description should go. Try and limit it to a paragraph or two, and maybe throw in a mention of what
PSRs you support to avoid any confusion with users and contributors.

### Packages

```
    "php": "~5.5|~7.0",
    "barryvdh/laravel-debugbar": "^2.2",
    "laravelcollective/html": "^5.2",
    "doctrine/dbal": "^2.5",
    "barryvdh/laravel-ide-helper": "^2.1",
    "maatwebsite/excel": "^2.1",
    "spatie/laravel-analytics": "^1.3",
    "spatie/laravel-medialibrary": "^3.17",
    "spatie/laravel-permission": "^1.3",
    "spatie/laravel-authorize": "^1.1",
    "spatie/geocoder": "^2.1",
    "mpociot/laravel-test-factory-helper": "^0.2.0",
    "laravel/socialite": "^2.0",
    "spatie/googlesearch": "^2.0"

    ----- devs ------

    "phpunit/phpunit": "4.*",
        "scrutinizer/ocular": "~1.1",
        "squizlabs/php_codesniffer": "~2.3",
        "laracasts/generators": "^1.1"
```

## Install

Via Composer

``` bash
$ composer require shawnsandy/laravel-install-kit
```
__Add to you__ `config/app.php -- providers`

``` php
    /*
    * Vendor Service Providers
    */
    Barryvdh\Debugbar\ServiceProvider::class,
    Collective\Html\HtmlServiceProvider::class,
    Barryvdh\LaravelIdeHelper\IdeHelperServiceProvider::class,
    Maatwebsite\Excel\ExcelServiceProvider::class,
```

__Add to__ `config/app.php -- aliases`

``` php
    'Debugbar' => Barryvdh\Debugbar\Facade::class,
    'Form' => Collective\Html\FormFacade::class,
    'Html' => Collective\Html\HtmlFacade::class,
    'Excel' => Maatwebsite\Excel\Facades\Excel::class,
```


## Usage


## Change log

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Testing

``` bash
$ composer test
```

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) and [CONDUCT](CONDUCT.md) for details.

## Security

If you discover any security related issues, please email shawnsandy04@gmail.com instead of using the issue tracker.

## Credits

- [shawn sandy][link-author]
- [All Contributors][link-contributors]

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/shawnsandy/laravel-install-kit.svg?style=flat-square
[ico-license]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square
[ico-travis]: https://img.shields.io/travis/LaravelToolKit/simple_pack/master.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/shawnsandy/laravel-install-kit.svg?style=flat-square

[link-packagist]: https://packagist.org/packages/shawnsandy/laravel-install-kit
[link-travis]: https://travis-ci.org/LaravelToolKit/simple_pack
[link-downloads]: https://packagist.org/packages/shawnsandy/laravel-install-kit
[link-author]: https://github.com/shawnsandy
[link-contributors]: ../../contributors
