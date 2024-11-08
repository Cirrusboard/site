---
title: Download
---

> ***NOTE:* Currently Cirrusboard is in development. It is not recommended to be used in a production environment yet, the database schema is subject to change, and does not have all features implemented yet.**

## System requirements
Some kind of web server with PHP and MySQL/MariaDB is needed. At least PHP 7.4 is required, but the latest version of PHP is recommended. Other than that Cirrusboard does not have any requirements. For more info see the [System requirements](System_Requirements) page.

## Distribution package
To install Cirrusboard, download the latest distribution package from GitHub CI, which has Composer dependencies and the default styling already compiled out of the box.

**(there should be some sort of download link here. for the time being you can check [here](https://github.com/Cirrusboard/Cirrusboard/actions) to grab the latest artifact)**

This package is ready to be pushed onto e.g. a shared hosting provider that doesn't support shell access.

## Clone source repository
For more advanced users, and those who may want to modify the source, it's recommended to clone the source repository:

```
git clone https://github.com/Cirrusboard/Cirrusboard
```

When doing this, you will have to manually install Composer dependencies and compile the default styling. If you're putting Cirrusboard on a shared hosting provider without shell access, you will need to do this preparation before pushing it onto production.

```
composer update -o
bash tools/compile-scss-sassc.sh
```

## Installing

### Web server configuration
Cirrusboard now uses a router script to route requests to the appropriate page. This also means that you will need to configure your web server to work with this. For Nginx, this is an example of what you would want to put in your configuration file.

```nginx
location / {
	try_files /static$uri /router.php?$args;
}
location /router.php {
	# include PHP-FPM here
}
```

For Apache, a `.htaccess` is provided which should work for running Cirrusboard under Apache. You will need to enable `mod_rewrite` for it to work.

### Setup
Currently, installation is done mostly manually. After having gotten Cirrusboard into the document root of your site and configured the web server, follow these steps:

1. Import the database dump inside `sql/` into a new database.

1. Copy `conf/config.sample.php` into `conf/config.php`, fill in your database credentials and specify the database you imported the dump into.

1. Make the `static/userpic/` and `templates/cache/` folders writeable by PHP.

After this is done, you should be able to access your newly installed forum. Please register an account immediately and before sharing the link to your forum, as the first registered user gets Root power of the forum.
