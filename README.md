<!--
SPDX-FileCopyrightText: 2021 Robin Vobruba <hoijui.quaero@gmail.com>

SPDX-License-Identifier: CC0-1.0
-->

# Rust project scripts

[![License: Unlicense](
    https://img.shields.io/badge/License-Unlicense-blue.svg)](
    https://unlicense.org)
[![REUSE status](
    https://api.reuse.software/badge/github.com/hoijui/rust-project-scripts)](
    https://api.reuse.software/info/github.com/hoijui/rust-project-scripts)

Scripts to build, test, clean and more for a simple Rust(lang) project,
useful for both local deving and CI.

## Usage

In your Rust(lang) project,
include this repo as a submodule:

```bash
git submodule add https://github.com/hoijui/rust-project-scripts.git scripts
```

From then on, you can use the scripts like this:

```bash
scripts/build
```

or

```bash
scripts/test
```

## Projects

Projects using these scripts:

* [`projvar`](https://github.com/hoijui/projvar/) -
  A tool that ensures that certain specific,
  project and build related environment variables are set.
* [`repvar`](https://github.com/hoijui/repvar/) -
  A tiny CLI tool that replaces variables of the style `${KEY}`
  in text with their respective value.
  It can also be used as a rust library.
* [`kicad-text-injector`](https://github.com/hoijui/kicad-text-injector/) -
  A tool that allows to post-process your KiCad PCB files,
  by replacing variables of the type `${KEY}` in your text elements.
