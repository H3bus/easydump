EasyDump
=====

EasyDump is an easy, sexy and lightweight way to display your PHP variable when developing. It is a nice alternative to ```var_dump```. It was partly inspired by (but not based on) [Kint](http://www.webresourcesdepot.com/kint-a-debugging-helper-for-php-apps/), but is way more simple.

## Use

### Dump variables

You only need the ```easydump.php``` file. Just include it in your code:

```php
require_once( 'easydump.php');
```

Then call the EasyDump functions:

```php
$var = 'test';
EasyDump::debug($var);     //just dump
EasyDump::debugExit($var); //exit code right after the dump
```

Or you can use the shortcut alias:

```php
d($var);
de($var);
```

See ```index.php``` for examples. The result would look like this:

![Screenshot of EasyDump](http://www.yosko.net/data/images/easydump.png) 

## Settings

Just change the values of the array called **$config** at the top of ```easydump.php``` :
- ```showVarNames```: show the variable names the way they were given during the EasyDump call (depends on SplFileObject, needs PHP 5.1.0+)
- ```showCall```: show the PHP code of the call to EasyDump (useful when doing a lot of dumps) (depends on SplFileObject, needs PHP 5.1.0+)
- ```color```: the HEX color theme for display

## Licence

EasyDump was thought and written to be in the public domain. This means you can do whatever you want with it without any restriction. If you need a public license, consider it as distributed under the [WTFPL](http://www.wtfpl.net/txt/copying/).

The only exception to this rule is the default color theme: it is called Earthsong and was originally created by [daylerees](https://github.com/daylerees/colour-schemes/#earthsong) and distributed under the MIT License.

Still, if you want to do a link to this page, it would be really appreciated :)
