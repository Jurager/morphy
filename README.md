# jurager/morphy

Laravel wrapper for phpMorphy library with PHP7 support

Source website (in russian): http://phpmorphy.sourceforge.net/  
SF project: http://sourceforge.net/projects/phpmorphy  
Wrapper on Github: https://github.com/juarager/morphy

This library allow retireve follow morph information for any word:
- Base (normal) form
- All forms
- Grammatical (part of speech, grammems) information

## Install

Via Composer
``` bash
$ composer require jurager/morphy
```

## Usage
``` php
$morphy = new jurager\morphy\Morphy('en');
echo $morphy->getPseudoRoot('FIGHTY');
```
## Laravel support
### Facade
``` php
Morphy::getPseudoRoot('БОЙЦОВЫЙ')
```

### Add russian facade support

Add to config/app.php:

Section ```providers```
``` php
jurager\morphy\MorphyServiceProvider::class,
```

Section ```aliases```
``` php
'Morphy'    => jurager\morphy\Facade\Morphy::class,
```

## Change log
Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Contributing
Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## Security
If you discover any security related issues, please email jurager01@gmail.com instead of using the issue tracker.

## License
The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
