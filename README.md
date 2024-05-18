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

Scripts to build, test, clean and more,
for a simple Rust(lang) project;
useful for both local dev'ing and CI.

By default, these scripts build using MUSL.
That means, that the resulting binary is usable
on any 64bit Linux system.
It also means, that we need some more tooling installed,
and that projects to be built have to be configured
to be MUSL buildable; the later mainly means,
choosing the right dependencies
and disabling features of deps. and sub-deps.

*Alternatively* you may also use Cargo directly, to make a simple,
local-system dependent build:

```sh
cargo build --release
```

## Usage

In your Rust(lang) project,
either:

1. include this repo as a submodule:

    ```bash
    git submodule add https://github.com/hoijui/rust-project-scripts.git run
    ```

2. or as an untracked, ignored dir (recommended):

    ```bash
    git clone https://github.com/hoijui/rust-project-scripts.git run
    if ! grep -q -r "^/run/\$" .git/info/exclude; then echo '/run/' >> .git/info/exclude; fi
    ```

From then on, you can use the scripts like this:

```bash
run/build
```

or

```bash
run/test
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
