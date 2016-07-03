# Laravel Install Kit

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Software License][ico-license]](LICENSE.md)
[![Build Status][ico-travis]][link-travis]
[![Total Downloads][ico-downloads]][link-downloads]
[![StyleCI](https://styleci.io/repos/55503103/shield)](https://styleci.io/repos/55503103)
[![SensioLabsInsight](https://insight.sensiolabs.com/projects/57f1441c-e839-40a5-9ebf-74c1afe3ee96/mini.png)](https://insight.sensiolabs.com/projects/57f1441c-e839-40a5-9ebf-74c1afe3ee96)


A simple Laravel PHP toolkit that contains and installs most of the Laravel packages that I regularly need to get ky laravel projects up and running. It replace the need for stater kits like laravel-hackaton-starter https://github.com/unicodeveloper/laravel-hackathon-starter, not that these are bad I just prefer to roll my own on top of fresh install of laravel  `laravel new blog` or `composer create-project --prefer-dist laravel/laravel blog`, just keeps me sane `;-)`.

### Packages

``` json

 "require": {
   "php": ">=5.5.9",
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
       "jeroen-g/laravel-packager": "^1.5",
       "laracasts/flash": "^2.0",
       "laracasts/generators": "^1.1",
       "cviebrock/eloquent-sluggable": "^3.1",
       "rap2hpoutre/laravel-log-viewer": "^0.6.0",
       "vinkla/hashids": "^2.2",
       "spatie/activitylog": "^2.4",
       "mews/purifier": "^2.0",
       "mcamara/laravel-localization": "^1.1",
       "barryvdh/laravel-elfinder": "^0.3.7",
       "greggilbert/recaptcha": "^2.1",
       "sven/artisan-view": "^1.0",
       "fedeisas/laravel-mail-css-inliner": "^1.4",
       "davejamesmiller/laravel-breadcrumbs": "^3.0",
       "sofa/revisionable": "^5.2",
       "graham-campbell/exceptions": "^8.4",
       "filp/whoops": "^2.1",
       "ipunkt/laravel-analytics": "^1.1",
       "anahkiasen/former": "^4.0",
       "proengsoft/laravel-jsvalidation": "^1.3",
       "evercode1/view-maker": "^3.4",
       "drawmyattention/laravel-make-resource": "~1.0",
       "anahkiasen/underscore-php": "^2.0","jeroen-g/laravel-packager": "^1.5",
       "arrilot/laravel-widgets": "^3.4"

  },

```
__Dev packages__ install on your own

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
    Laravel\Socialite\SocialiteServiceProvider::class,
    Barryvdh\Debugbar\ServiceProvider::class,
    Collective\Html\HtmlServiceProvider::class,
    Barryvdh\LaravelIdeHelper\IdeHelperServiceProvider::class,
    Maatwebsite\Excel\ExcelServiceProvider::class,
    Spatie\LaravelAnalytics\LaravelAnalyticsServiceProvider::class,
    Spatie\Authorize\AuthorizeServiceProvider::class,
    Spatie\Permission\PermissionServiceProvider::class,
    Spatie\MediaLibrary\MediaLibraryServiceProvider::class,
    Spatie\Geocoder\GeocoderServiceProvider::class,
    Spatie\Activitylog\ActivitylogServiceProvider::class,
    Mpociot\LaravelTestFactoryHelper\TestFactoryHelperServiceProvider::class,
    Styde\Html\HtmlServiceProvider::class,
    Cviebrock\EloquentSluggable\SluggableServiceProvider::class,
    Rap2hpoutre\LaravelLogViewer\LaravelLogViewerServiceProvider::class,
    Vinkla\Hashids\HashidsServiceProvider::class,
    Mews\Purifier\PurifierServiceProvider::class,
    Mcamara\LaravelLocalization\LaravelLocalizationServiceProvider::class,
    Barryvdh\Elfinder\ElfinderServiceProvider::class,
    Greggilbert\Recaptcha\RecaptchaServiceProvider::class,
    Sven\ArtisanView\ArtisanViewServiceProvider::class,
    Vinkla\Hashids\HashidsServiceProvider::class,
    Fedeisas\LaravelMailCssInliner\LaravelMailCssInlinerServiceProvider::class,
    DaveJamesMiller\Breadcrumbs\ServiceProvider::class,
    Kris\LaravelFormBuilder\FormBuilderServiceProvider::class,
    JeroenG\Packager\PackagerServiceProvider::class,
    Sofa\Revisionable\Laravel\ServiceProvider::class,
    GrahamCampbell\Exceptions\ExceptionsServiceProvider::class,
    Ipunkt\LaravelAnalytics\AnalyticsServiceProvider::class,
    Sven\EnvProviders\EnvServiceProvider::class,
    Prettus\Repository\Providers\RepositoryServiceProvider::class,
    InfyOm\Generator\InfyOmGeneratorServiceProvider::class,
    InfyOm\CoreTemplates\CoreTemplatesServiceProvider::class,
    Former\FormerServiceProvider::class,
    Proengsoft\JsValidation\JsValidationServiceProvider::class,
    Evercode1\ViewMaker\ViewMakerServiceProvider::class,

    ]
```

__Aliases__ `config/app.php -- aliases`

``` php

$aliases => [

    /*
     * Vendor aliases
     */
    'Debugbar' => Barryvdh\Debugbar\Facade::class,
    'Html' => Collective\Html\HtmlFacade::class,
    'Geocoder' => Spatie\Geocoder\GeocoderFacade::class,
    'LaravelAnalytics' => Spatie\LaravelAnalytics\LaravelAnalyticsFacade::class,
    'Excel' => Maatwebsite\Excel\Facades\Excel::class,
    'Alert' => Styde\Html\Facades\Alert::class,
    'Field' => Styde\Html\Facades\Field::class,
    'Menu' => Styde\Html\Facades\Menu::class,
    'Hashids' => Vinkla\Hashids\Facades\Hashids::class,
    'Purifier' => Mews\Purifier\Facades\Purifier::class,
    'LaravelLocalization'   => Mcamara\LaravelLocalization\Facades\LaravelLocalization::class,
    'Recaptcha' => Greggilbert\Recaptcha\Facades\Recaptcha::class,
    'Hashids' => Vinkla\Hashids\Facades\Hashids::class,
    'Tracker' => PragmaRX\Tracker\Vendor\Laravel\Facade::class,
    'Breadcrumbs' => DaveJamesMiller\Breadcrumbs\Facade::class,
    'FormBuilder' => Kris\LaravelFormBuilder\Facades\FormBuilder::class,
    'Socialite' => Laravel\Socialite\Facades\Socialite::class,
    'Analytics' => Ipunkt\LaravelAnalytics\AnalyticsFacade::class,
    'Former' => 'Former\Facades\Former',
    'JsValidator' => Proengsoft\JsValidation\Facades\JsValidatorFacade::class,


    ]

```

__Middleware__

``` php
    protected $middleware = [
        //...
        \Styde\Html\Alert\Middleware::class,
        //...
    ];
```

__Middleware (Route)__ `app/Http/Kernel.php`

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

# Usage

## Packages / Artisan Commands

__Laravel Debugbar__

``` bash
    php artisan vendor:publish --provider="Barryvdh\Debugbar\ServiceProvider"
```

__StydeNet Html__ https://github.com/StydeNet/html

``` bash
    php artisan vendor:publish --provider='Styde\Html\HtmlServiceProvider'
```

__Laravel Packages__ https://github.com/Jeroen-G/laravel-packager

__Laravel 5 IDE Helper Generator__ https://github.com/barryvdh/laravel-ide-helper

``` bash
    php artisan vendor:publish --provider="Barryvdh\LaravelIdeHelper\IdeHelperServiceProvider" --tag=config
```

__Laravel Analytics__ https://github.com/spatie/laravel-analytics

``` bash


    php artisan vendor:publish --provider="Spatie\LaravelAnalytics\LaravelAnalyticsServiceProvider"


```

__Laravel Media Library__ https://github.com/spatie/laravel-medialibrary

``` bash

    php artisan vendor:publish --provider="Spatie\MediaLibrary\MediaLibraryServiceProvider" --tag="migrations"

```

__Laravel Authorize__ https://github.com/spatie/laravel-authorize

``` bash

    php artisan vendor:publish --provider="Spatie\Authorize\AuthorizeServiceProvider"

```

__Laravel Geocoder__ https://github.com/spatie/geocoder

``` bash

    php artisan vendor:publish --provider="Spatie\Authorize\AuthorizeServiceProvider"

```

__Laravel Test Factory Generator__ https://github.com/mpociot/laravel-test-factory-helper

__Laravel Google Search__ https://github.com/spatie/googlesearch

``` bash

     php artisan vendor:publish --provider="Spatie\GoogleSearch\GoogleSearchServiceProvider"

 ```

__Laravel Flash__ https://github.com/laracasts/flash

__Eloquent-Sluggable__ https://github.com/cviebrock/eloquent-sluggable

__Laravel log viewer__ https://github.com/rap2hpoutre/laravel-log-viewer

__Laravel Hashids__ https://github.com/vinkla/hashids

__Laravel Activity Log__ https://github.com/spatie/activitylog

__Laravel Localization__ https://github.com/spatie/activitylog

__Laravel Localization__ https://github.com/spatie/activitylog

__Laravel elFinder__ https://github.com/barryvdh/laravel-elfinder

__Laravel elFinder__ https://github.com/barryvdh/laravel-elfinder

__Google ReCaptcha__ https://github.com/greggilbert/recaptcha

__Laravel Mail CSS-Inliner__ https://github.com/fedeisas/laravel-mail-css-inliner

__Laravel Bread Crumbs__ https://github.com/davejamesmiller/laravel-breadcrumbs

__Sofa/Revionable__ https://github.com/jarektkaczyk/revisionable

__Laravel Exceptions__ https://github.com/GrahamCampbell/Laravel-Exceptions

__Laravel Analytics__ https://github.com/ipunkt/laravel-analytics

__Laravel EnvProviders__ https://github.com/svenluijten/env-providers

__Former__ https://github.com/formers/former

__Laravel JsValidation__ https://github.com/proengsoft/laravel-jsvalidation

__View Maker__ https://github.com/evercode1/view-maker

ViewMaker is for use with the Laravel PHP framework (5.2 and up) Artisan command line tool.

ViewMaker adds 10 new artisan commands, providing ready-made templates for CRUD generation, Views and Datagrids, with ajax-powered search, column sorts and pagination. You can create and test a foundation of code with crud and views in under a minute.

## Recommend Packages

__Laravel Generators__ http://labs.infyom.com/laravelgenerator/docs/getting-started/installation


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
