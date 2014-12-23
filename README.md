# Iota [![Build Status](https://travis-ci.org/gchp/iota.svg?branch=master)](https://travis-ci.org/gchp/iota)

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/gchp/iota?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Iota is a terminal-based text-editor written in Rust.

Here's what it looks like right now, editing itself.

![Screenshot](https://raw.githubusercontent.com/gchp/iota/master/screenshot.png)

## Motivation

Iota was born out of my frustrations with existing text editors. Over the years I've tried
combinations of simple text editors, IDEs and everything in between. None of them felt right
to me, however. Some were too slow & bulky, others were too difficult to customise and still
others were platform specific and I couldn't use them on all my machines.

I started building Iota with the view of combining ideas and features from serveral different
editors while designing it to work on modern hardware.

Why Rust? Because its fun and why not!

## Goals

The goals for Iota are that it would be:

- 100% open source
- highly extensible/customisable/scriptable
- fast & efficient - designed with modern hardware in mind
- cross platform - it should work anywhere
- developer friendly - it should just "get out of the way"
- Rust tooling integration (see note below)

Iota is still in the very early stages, and is probably not ready for every day use.
Right now the focus is on implementing and polishing the basic editing functionality.

Windows support is coming, but it's somewhat slow right now. Help with this would
be greatly appreciated!

**Note on Rust integration:**
_The aim is to support code editing in all languages (and of course plain text),
with a lean towards Rust and integration with Rust tools. I don't intend it to
be a "Rust IDE" or "Rust only", however I think it would be cool to experiment with
integration with Rust tooling. This could also be applied to other languages too._

## Usage

Clone the project and run `cargo build`.

Then to start the editor run `./target/iota /path/to/file.txt`. Or simply `./target/iota`
to open an empty buffer.

You can also create buffers from `stdin`.

```bash
# open a buffer with the output of `ifconfig`
ifconfig | ./target/iota
```

You can move the cursor around with the arrow keys.

To save, press `Ctrl-s`.
To exit, press `Ctrl-q`.

Iota currently supports Emacs-style keybindings for simple movement.

- `Ctrl-p` move up
- `Ctrl-n` move down
- `Ctrl-b` move backwards
- `Ctrl-f` move forwards
- `Ctrl-a` move to start of line
- `Ctrl-e` move to end of line
- `Ctrl-d` delete forwards
- `Ctrl-h` delete backwards
- `Ctrl-q` quit
- `Ctrl-s` save
- `Ctrl-y` undo
- `Ctrl-z` redo

There are also plans to optionally enable Vi-like keybindings & modes.
