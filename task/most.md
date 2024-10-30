# most

- MOST_EDITOR > SLANG_EDITOR > EDITOR
- MOST_INITFILE
- MOST_SWITCHES
- MOST_HELP

`most` uses the following environment variables:

## MOST_SWITCHES

This variable is used to specify commonly used options. For example, some people prefer to use `most` with the `-s` option so that excess blank lines are not displayed. `export MOST_SWITCHES='-s'`.

## MOST_INITFILE

Set this variable to specify the initialization file to load during startup. The default action is to load the system config file from `/etc/most.conf` and then a personal config file located at `$HOME/.mostrc`.

`MOST_INITFILE` specifies a configuration file for MOST. One can specifiy keymaps, colors, etc. via this file. In the absence of MOST_INITFILE, the program will look for a file call `.mostrc` in the home directory. See `lesskeys.rc` for an example of a key definition file that causes MOST to emulate the `less` pager. See also `most-fun.txt` for a list of functions that can be used for key definitions. The file `most.rc` list the bindings that are built-in to the viewer.

## MOST_EDITOR

Either of these environment variables specify an editor for most to invoke to edit the file. The value can contain `%s` (represents file name) and `%d` (represents line number) formatting descriptors. For example, if 'jed' is your editor, you may set `MOST_EDITOR='jed %s -g %d'`. If MOST_EDITOR is not found, 'most' looks for `SLANG_EDITOR`, then for `EDITOR`. The key `e` calls the editor, but read-only pages, like man pages, cannot be edited like this (but no message is shown).

`MOST_EDITOR` and `SLANG_EDITOR` are formatted strings describing what editor to use. The string can contain %s and %d formatting descriptors that represent the file name and line number, respectively. For example, if JED is your editor, then set MOST_EDITOR to 'jed %s -g %d'. Since MOST is just one of several programs that use the S-Lang library, I suggest that you use `SLANG_EDITOR` instead of MOST_EDITOR.

## MOST_HELP

This variable may be used to specify an alternate help file.
If `MOST_HELP` is defined to point to an existing file, MOST will load that file as a help file. This is useful for describing custom keymaps.
