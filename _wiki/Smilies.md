---
title: Smilies
---
Cirrusboard supports the ability to convert text strings into small images in posts, i.e. smilies.

By default, Cirrusboard comes with no smilies out of the box, but [a repository of smilies is available on GitHub](https://github.com/Cirrusboard/Cirrusboard-smilies).

The smiley definition is an array of smilies called `$smilies` in the config file. The key is the smiley code and the value is the image. For example:

```php
$smilies = [
	':)' => 'smilies/smile.png',
];
```

To install smilies from the repository, you would copy the PHP array code into your configuration file, and copy the smiley images into `static/smilies/`.
