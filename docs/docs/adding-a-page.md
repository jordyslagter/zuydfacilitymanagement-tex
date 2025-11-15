---
sidebar_position: 5
---

# Adding a page to your document

In this example we will add the page 'Results'.

## Adding the file

First, add the a new `.tex` file to either the `frontmatter`,
`mainmatter` or `appendix` directories based on what kind of page it is.

In our example we will create the `mainmatter/results.tex` file.

## Linking it to main.tex

Next, let's link it to `main.tex` so that it actually shows up in our
document. Open `main.tex` and this is what you should see:

```tex
%!TEX program = lualatex
\documentclass{zuydfacilitymanagement}
\input{packages}
\input{metadata}
\input{cover}

\begin{document}
  % \makecoverandtitle automatically starts roman numbering, when not using
  % this command use \frontmatter to start roman numbering
  \makecoverandtitle

  % include any of your own pages using \include{frontmatter/page}
  \include{frontmatter/0-voorwoord}
  \include{frontmatter/1-samenvatting}

  \tableofcontents

  \mainmatter % start arabic numbering

  % include any of your own pages using \include{mainmatter/page}
  \include{mainmatter/0-inleiding}
  \include{mainmatter/1-methode}

  \printbibliography

  \appendix

  % include any of your own pages using \include{appendix/page}
  \include{appendix/bijlage1}
  \include{appendix/bijlage2}
\end{document}
```

We want to add our results page to the mainmatter, so let's add it under the
`mainmatter` command. This ensures it gets placed properly and gets the
correct numbering system required by the document specification.

```tex
\mainmatter % start arabic numbering

% include any of your own pages using \include{mainmatter/page}
\include{mainmatter/0-inleiding}
\include{mainmatter/1-methode}
\include{mainmatter/results} % <-- we add it right here!
```

Now your entire document should look like this:

```tex
%!TEX program = lualatex
\documentclass{zuydfacilitymanagement}
\input{packages}
\input{metadata}
\input{cover}

\begin{document}
  % \makecoverandtitle automatically starts roman numbering, when not using
  % this command use \frontmatter to start roman numbering
  \makecoverandtitle

  % include any of your own pages using \include{frontmatter/page}
  \include{frontmatter/0-voorwoord}
  \include{frontmatter/1-samenvatting}

  \tableofcontents

  \mainmatter % start arabic numbering

  % include any of your own pages using \include{mainmatter/page}
  \include{mainmatter/0-inleiding}
  \include{mainmatter/1-methode}
  \include{mainmatter/results}

  \printbibliography

  \appendix

  % include any of your own pages using \include{appendix/page}
  \include{appendix/bijlage1}
  \include{appendix/bijlage2}
\end{document}
```

## Giving it a title

The zuydfacilitymanagement $ \LaTeX $ class exposes three types of chapters:

- `\chapter`
- `\unnumberedchapter`
- `\notocchapter`

In this case, we want the regular `\chapter`, as it gives us a number and adds
it to the table of contents for us.

Let's go back to `results.tex`, and add the following:

```tex
\chapter{Results}
```

You should now see that in your document, a new chapter has appeared with the
title 'Results', it has been added to your table of contents with the correct
page number and everything!
