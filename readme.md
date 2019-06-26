# TCKimlikNo

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Total Downloads][ico-downloads]][link-downloads]
[![Build Status][ico-travis]][link-travis]
[![Quality Score][ico-scrutinizer]][link-scrutinizer]
[![StyleCI][ico-styleci]][link-styleci]

Turkish Identification Number Verification & Validation Package for Laravel.

## Installation

Via Composer

``` bash
$ composer require deligoez/tckimlikno
```

If you are using Laravel 5.5+, the package will automatically register the service provider for you.

If you are using Lumen, you will need to add the following to bootstrap\app.php:

``` php
\\ Register Service Providers
$app->register(Deligoez\TCKimlikNo\TCKimlikNoServiceProvider::class);
```

## Usage

``` php
use Deligoez\TCKimlikNo\TCKimlikNo;


// Verifies Citizenship Number According to it's Algorithm.
// Returns Boolean
TCKimlikNo::verify('12345678901');

// Verifies Parameters and validates all using nvi.gov.tr API
// Returns Boolean
TCKimlikNo::validate('10000000146', 'Yunus Emre', 'Deligöz', '1900')
// Auto Uppercase Disabled
TCKimlikNo::validate('10000000146', 'YUNUS EMRE', 'DELİGÖZ', '1900', false)
```

## Change log

Please see the [changelog](changelog.md) for more information on what has changed recently.

## Testing

``` bash
$ composer test
```

## Contributing

Please see [contributing.md](contributing.md) for details and a todolist.

## Security

If you discover any security related issues, please email ye@deligoz.me instead of using the issue tracker.

## Credits

- [Yunus Emre Deligöz][link-author]
- [All Contributors][link-contributors]

## License

MIT. Please see the [license file](license.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/deligoez/tckimlikno.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/deligoez/tckimlikno.svg?style=flat-square
[ico-travis]: https://img.shields.io/travis/deligoez/tckimlikno/master.svg?style=flat-square
[ico-styleci]: https://styleci.io/repos/193854934/shield
[ico-scrutinizer]: https://img.shields.io/scrutinizer/g/deligoez/tckimlikno.svg?style=flat-square

[link-packagist]: https://packagist.org/packages/deligoez/tckimlikno
[link-downloads]: https://packagist.org/packages/deligoez/tckimlikno
[link-travis]: https://travis-ci.org/deligoez/tckimlikno
[link-styleci]: https://styleci.io/repos/193854934
[link-scrutinizer]: https://scrutinizer-ci.com/g/deligoez/tckimlikno
[link-author]: https://github.com/deligoez
[link-contributors]: ../../contributors
