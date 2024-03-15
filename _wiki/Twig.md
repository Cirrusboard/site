---
title: Twig
---

Twig is the name of the templating engine used by Cirrusboard. For documentation about Twig, see [their website](https://twig.symfony.com/doc/3.x/).

All pages in Cirrusboard use the `twigloader()` function which loads Twig along with Cirrusboard-specific extensions. Templates are read from the `templates/` directory.

Previously you had to clear the template cache for changes in Twig templates to show. This is no longer necessary and changes will now take effect immediately.
