---
sidebar_position: 6
---

# Available commands

This page simply describes all exposed commands by the zuydfacilitymanagement
document class.

## `\chapter`

Generates a chapter with a title, number, and adds it to the table of contents.

Usage:

```tex
\chapter{Chapter name}
```

## `\unnumberedchapter`

Generates a chapter with a title, _no_ number, and adds it to the table of
contents.

Usage:

```tex
\unnumberedchapter{Chapter name}
```

## `\notocchapter`

Generates a chapter with a title, _no_ number, and _does not_ add it to the
table of contents.

Usage:

```tex
\notocchapter{Chapter name}
```

## `\blankpage`

Generates a completely blank page that skips a page number.

Usage:

```tex
\blankpage
```

## `\frontmatter`

Starts numbering the pages with roman numerals.

Usage:

```tex
\frontmatter
```

## `\mainmatter`

Starts numbering the pages with arabic numerals.

Usage:

```tex
\mainmatter
```

## `\appendix`

Starts numbering the chapters alphabetically and adds a blank page with
'Bijlagen' displayed in the middle.

Usage:

```tex
\appendix
```

## `\cover`

Removes the default cover and replaces it with the one defined in this command
this can be used to create your own cover, but is rather advanced. Support
is provided for `pagecolor` and `color`.

```tex
\cover{
  My own cover page!\\
  A second line!
}
```

## `\@variable`

These can be used to access applied variables yourself. This can be useful when
designing your own cover page. They map one-to-one to the variables defined in
the metadata page.

Usage:

```tex
\@title
\@subtitle
\@professor
% etc...
```
