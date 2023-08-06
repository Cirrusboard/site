---
title: Configuration
---
Cirrusboard is mainly configured through files inside of the `conf/` folder. For each configuration file, there's a sample configuration you can copy to customise to your liking.

The configuration files are PHP files, which mean you can configure things programmatically if desired.

## `config.php`
Main configuration file.


## `faq.php`
Defines the text in the FAQ. The default sample FAQ provides some default content, including a sane set of rules and policies.

The format is a single variable named `$faq`, an array of FAQ entries of which have the fields `id`, `title` and `content`. See the sample configuration for an example of how to lay it out.

There are some predefined variables you can make use of inside the FAQ:
- `$smileytable`: Table with the smilies currently defined.
- `$nctable`: Table with nickname colours. Needs to be enclosed inside table tags.