# Laravel Install Kit

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Software License][ico-license]](LICENSE.md)
[![Build Status][ico-travis]][link-travis]
[![Total Downloads][ico-downloads]][link-downloads]

A simple toolkit that contains and installs most of the Laravel packages I need to get you up and running quickly on PHP projects.

### Packages

``` php

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
    "spatie/googlesearch": "^2.0",
    "styde/html": "~1.1",
    "laracasts/utilities": "^2.1",
    "jeroen-g/laravel-packager": "^1.4",
    "laracasts/flash": "^2.0",

```
__Dev packages__ install on your ows

``` php

    "laracasts/generators": "^1.1"

```

## Install

Via Composer

``` bash
$ composer require shawnsandy/laravel-install-kit
```
__Providers__ `config/app.php -- providers`

``` php
$providers => [

    /*
    * Vendor Service Providers
    */
    Barryvdh\Debugbar\ServiceProvider::class,
    Collective\Html\HtmlServiceProvider::class,
    Barryvdh\LaravelIdeHelper\IdeHelperServiceProvider::class,
    Maatwebsite\Excel\ExcelServiceProvider::class,
    Spatie\LaravelAnalytics\LaravelAnalyticsServiceProvider::class,
    Spatie\Authorize\AuthorizeServiceProvider::class,
    Spatie\Permission\PermissionServiceProvider::class,
    Spatie\MediaLibrary\MediaLibraryServiceProvider::class,
    Spatie\Geocoder\GeocoderServiceProvider::class,
    Mpociot\LaravelTestFactoryHelper\TestFactoryHelperServiceProvider::class,
    Styde\Html\HtmlServiceProvider::class,
    Cviebrock\EloquentSluggable\SluggableServiceProvider::class,
    Rap2hpoutre\LaravelLogViewer\LaravelLogViewerServiceProvider::class,

    ]
```

__Aliases__ `config/app.php -- aliases`

``` php

$aliases => [

    /*
     * Vendor aliases
     */
    'Debugbar' => Barryvdh\Debugbar\Facade::class,
    'Form' => Collective\Html\FormFacade::class,
    'Html' => Collective\Html\HtmlFacade::class,
    'Geocoder' => Spatie\Geocoder\GeocoderFacade::class,
    'LaravelAnalytics' => Spatie\LaravelAnalytics\LaravelAnalyticsFacade::class,
    'Excel' => Maatwebsite\Excel\Facades\Excel::class,
    'Alert' => Styde\Html\Facades\Alert::class,
    'Field' => Styde\Html\Facades\Field::class,
    'Menu' => Styde\Html\Facades\Menu::class,

    ]
```

__Middleware__ `app/Http/Kernel.php`

``` php

protected $routeMiddleware = [
  ...
  'can' => \Spatie\Authorize\Middleware\Authorize::class,
];

```

__Providers__

```
    /**
       * Register any application services.
       *
       * @return void
       */
      public function register()
      {
          /*
           * Custom providers
           */
          if ($this->app->environment() == 'local') {
              $this->app->register('Laracasts\Generators\GeneratorsServiceProvider');
          }
      }

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
