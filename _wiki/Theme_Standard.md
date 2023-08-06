---
title: Theme Standard
---
The Cirrusboard theme standard is derived from Acmlmboard, and is largely compatible albeit with some tweaks.

## Directory structure
Each theme is in its own folder in `themes/`. The stylesheet file should be called `style.css`, and any accompanying images and other assets should be put next to it in the theme's folder. Every theme should have a `meta.json` containing metadata about the theme. Check the built in theme's `meta.json` file for the values required.

## Defaults
- Open Sans is the default font
- By default links are lime-ish green
- Background colour is black, text colour is white.

## Classes

### `<table>`
- `table.c1`: All layout tables.

### `<tr>`
- `tr.h`: Header row.
- `tr.c`: Subheader row.

### `<td>`
- `td`: Any layout table cell. Usually used to give a border.
	- In Acmlmboard, this was called `td.b`, but all cells are "bordered" by default in Cirrusboard.
- `td.nb`: "No border", override any border value.

### "Zebra"
- `.n1`, `.n2`, `.n3`: "Zebra" classes, used for the differing colours in table rows.

### Misc.
- `.sfont`: Class used to make text smaller.
- `.reglog div`: The separator used in register/login pages. Use `border-top: 1px solid $primary;` to customise it.
- `.quote .quotetext`: The horizontal borders in quote blocks. Use `border: 2px solid $primary;` to customise it. (common CSS already set vertical borders to 0)

## Other
Apart from these "public" classes you can of course also override or play with "internal" classes defined in the common CSS styling.