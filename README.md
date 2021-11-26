# Termbox

Termbox is a library for creating Text User-Interfaces (TUIs). It represents the
terminal as a grid of cells, where each cell contains a glyph. It's a decent
and simple alternative to curses!

## Installation

As standard for single-header libraries:

1. Put `termbox.h` in your source tree.
2. Define `_TERMBOX_IMPL` in at least one file that includes `termbox.h`
3. Optionally, if you have a system definition of `wcwidth` or otherwise don't
   need the definition in the header, define `_TERMBOX_NOWCWIDTH`

## Getting started

Termbox's interface only consists of 12 functions:

```
tb_init() // initialization
tb_shutdown() // shutdown

tb_width() // width of the terminal screen
tb_height() // height of the terminal screen

tb_clear() // clear buffer
tb_present() // sync internal buffer with terminal

tb_put_cell()
tb_change_cell()
tb_blit() // drawing functions

tb_select_input_mode() // change input mode
tb_peek_event() // peek a keyboard event
tb_poll_event() // wait for a keyboard event
```

See src/termbox.h header file for full detail.

## History

In the beginning was the Library, and the Library was Termbox. Termbox was Good.
Termbox was a simple alternative to ncurses, with bindings in many languages.

However, I never did like worrying about SOs and As and Cs and INLs! Since the
sea change in C changes brought about by the great idea of single-header
libraries, I don't have to (except for huge things like SDL and PCRE). Termbox
was never a big library, and it's basically complete now (or at least
unmaintained), so... let's make it into a single-header library, yay!

## Links

If you want me to add your Termbox project here, send me a pull request.

### Language bindings

- https://github.com/nsf/termbox - Python
- https://github.com/adsr/termbox-php - PHP
- https://github.com/gchp/rustbox - Rust
- https://github.com/fouric/cl-termbox - Common Lisp
- https://github.com/zyedidia/termbox-d - D
- https://github.com/dduan/Termbox - Swift
- https://github.com/andrewsuzuki/termbox-crystal - Crystal
- https://github.com/jgoldfar/Termbox.jl - Julia
- https://github.com/mitchellwrosen/termbox - Haskell
- https://github.com/dom96/nimbox - Nim
- https://github.com/ndreynolds/ex_termbox - Elixir
- https://github.com/bmsauer/termbox-ada - Ada
- https://github.com/luxint/termbox - newLISP

### Other implementations

- https://github.com/nsf/termbox-go - Go pure Termbox implementation

### Applications

- https://github.com/adsr/mle - a small, flexible terminal-based text editor
- https://github.com/colinta/Ashen - framework for building terminal applications based on the Elm architecture
- https://github.com/afify/sfm - simple file manager for unix-like systems

## Bugs & questions

Report bugs to the https://github.com/japanoise/termbox issue tracker.
