---
sidebar_position: 2
---

# Compiling

The Zuyd Facility Management document class _requires_ using XeTeX or LuaTeX.
The default pdfTeX compiler is _not supported_!

In Overleaf, you can ensure that XeTeX or LuaTeX is used by going into the
sidebar and selecting either.

In all TeX distributions discussed in [Getting started](./getting-started.md)
you can include something called a 'magic comment' at the top of the
`main.tex` file. This should be included by default, but if not you can do
this yourself by adding the following:

```tex
%!TEX program = lualatex
```

Again, ensure this is at the top of the `main.tex` file!
