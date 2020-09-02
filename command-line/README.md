# Command Line

## Notes

These notes are based on PyBites's "[PyBites Developer Tools Workshop](https://pybit.es/pages/devtools)" tutorial:

- [Ag](https://github.com/ggreer/the_silver_searcher) (a.k.a. The Silver Searcher):
  - It is a code searching tool (it works as an alternative to `find` and `grep`).
  - It allows, for example, to search for a certain term in the various files of a project and check a preview of each one of them on the command line.
  - Limit your search to Python files (`.py`): `alias agg='ag --python'`.
  - Check the list of available file types (_filters_): `ag --list-file-types` (or [here](https://github.com/ggreer/the_silver_searcher/blob/master/tests/list_file_types.t)).
- [fzf](https://github.com/junegunn/fzf):
  - It is a tool for fast file navigation.
