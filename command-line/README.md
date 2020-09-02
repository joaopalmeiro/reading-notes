# Command Line

## Notes

These notes are based on PyBites's "[PyBites Developer Tools Workshop](https://pybit.es/pages/devtools)" training session:

- [Ag](https://github.com/ggreer/the_silver_searcher) (a.k.a. The Silver Searcher):
  - It is a code searching tool (it works as an alternative to `find` and `grep`).
  - It allows, for example, to search for a certain term in the various files of a project and check a preview of each one of them on the command line.
- [fzf](https://github.com/junegunn/fzf):
  - It is a tool for fast file navigation.
- [howdoi](https://github.com/gleitz/howdoi):
  - It is a command line tool to get answers from Stack Overflow for a given query.
  - It can also be used as a Python package.
- [cmder](https://cmder.net/):
  - It is a console emulator for Windows.
- [tmux](https://github.com/tmux/tmux):
  - It is a terminal multiplexer.
  - Basically, it allows multiple terminal sessions in a single window.

## Commands

- Ag:
  - Check the list of available file types (_filters_): `ag --list-file-types` (or [here](https://github.com/ggreer/the_silver_searcher/blob/master/tests/list_file_types.t)).

## Aliases

- Ag:
  - Limit your search to Python files (`.py`): `alias agg='ag --python'`.
- `ls` command with file sizes in a human-readable format and with entries sorted from oldest to most recent: `alias lt='ls -lrth'`.
- `alias brc='code ~/.bashrc'` (file to add aliases).
