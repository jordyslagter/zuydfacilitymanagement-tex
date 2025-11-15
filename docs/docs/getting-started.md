---
sidebar_position: 1
---

# Getting started

This document details the needed prerequisites and steps needed to set up a new
$ \LaTeX $ document using the zuydfacilitymanagement class.

## Prerequisites

- Either a local or remote (Overleaf) environment to run $ \LaTeX $ in.
- The Zuyd style font 'Avenir Next LT Pro' regular, italic and bold installed
  on your system and available.

It is recommended to use a local environment for this project as Overleaf
quickly runs out of compilation space on the free plan. Overleaf, however,
is still recommended for non-CS students that don't know alternative
decentralised collaboration tools such as Git.

### Setting up a local environment

#### MacOS

Using [brew](https://brew.sh), install the following:

```bash
brew install mactex
```

#### Linux

Using your distro's package manager, install TeX Live.

Arch-based:

```bash
pacman -S texlive
```

#### Windows

Using [scoop](https://scoop.sh), install MikTeX.

```bash
scoop install miktex
```

### Using Overleaf

Navigate to the official [Overleaf](https://overleaf.com) or a self-hosted
version and create a new blank project.

### Avenir Next LT Pro font

The Avenir Next LT Pro font is property of Microsoft and thus cannot be
distributed via these pages. It can be legally installed to your system using
Microsoft Word with the license tied to your Zuyd University account.

Otherwise, well, I certainly would never endorse going to
[duckduckgo](https://duckduckgo.com) and typing in the prompt
'Avenir LT Pro font free'. I would never. Do you think I'm some kind of cowboy?

Make sure you have regular, bold and italic installed and available.

## Downloading the document template

Navigate to the
[releases](https://github.com/jordyslagter/zuydfacilitymanagement-tex/releases)
and download the latest `.zip` file to your computer. Place it somewhere where
you can find it again and unzip using a tool like unzip (Linux) or
[7-Zip](https://7-zip.org) (Windows).
