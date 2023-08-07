---
title: Twig
---

Twig is the name of the templating engine used by Cirrusboard. For documentation about Twig, see [their website](https://twig.symfony.com/doc/3.x/).

All pages in Cirrusboard use the `twigloader()` function which loads Twig along with Cirrusboard-specific extensions. Templates are read from the `templates/` directory.

## Clearing Twig cache
Twig works by compiling the template files into raw PHP that then gets executed. These compiled files can be cached to reduce the overhead of the templating engine. This also means that changes you make to the Twig templates won't immediately take effect unless you clear the Twig cache. If your Twig cache is at the default location, then `./tools/clear-cache.sh` can be used to clear it.

If you're doing more serious development then you would want to set `$tplNoCache` which completely disables the cache and will always compile the template.
