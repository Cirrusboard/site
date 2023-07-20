---
title: System Requirements
---
Cirrusboard requires a regular PHP & MySQL web stack to run on.

## Web server
Obviously, you will need a web server. Practically any web server that has the ability to run PHP scripts should work, whether it be nginx, Apache or something else out there.

## PHP
Cirrusboard is written in PHP, and as such requires PHP to be installed on the server. PHP 7.4 is currently the minimum version which should work but the latest version is always recommended.

No additional extensions are required, but the OPCache Zend extension is recommended for a performance boost. Usually this comes by default with your distribution's PHP package.

## MySQL/MariaDB
Cirrusboard relies on a MySQL/MariaDB database. Practically any relatively recent version should work.

## Hardware requirements
Practically anything that can handle a LEMP stack should work, from a low-end Pi to a cheap VPS. Basically anything with 250MB RAM or more, a couple megabytes to spare, and a CPU.
