---
title: Security
---
Cirrusboard has been written to be as secure as possible, with all common attack vectors of a web application taken in mind. It has also been tested in a production scenario on Voxelmanip Forums and proven to be reasonably secure.

## SQL injection
All queries in Cirrusboard that contain user input are constructed with prepared statements, making SQL injection close to impossible.

## XSS
Cirrusboard makes use of the Twig templating engine, which treats all variables passed to the template as unsafe by default and sanitises them.

When HTML is disabled, all posts will be sanitised making XSS in posts impossible. When HTML is enabled, a reasonable attempt to prevent JavaScript or other dangerous HTML elements from being put in posts.

Cirrusboard also makes use of a CSP which is enforced by the client's browser to prevent any inline or external JavaScript from being run. The only JavaScript files that can be run are ones local to the website, which includes Cirrusboard's own JavaScript code. External stylesheets and font files are also restricted.

## Arbitrary PHP execution
No `eval()` (more like `evil()`!) is used in the code.

**However**, if your web server is misconfigured PHP code might be able to be executed in profile pictures. You should make sure you have set up PHP in the proper way, which should never run PHP code for files without the .php extension (which profile pictures do not have).

## Disclaimer
No software is perfect, and mistakes may happen, whether it be caused by your configuration or Cirrusboard itself. As stated in the license Cirrusboard is provided **AS IS** without any warranty.

If you believe you have found a vulnerability in the Cirrusboard software, please responsibly disclose it privately to [ROllerozxa](https://voxelmanip.se/about/#contact).
