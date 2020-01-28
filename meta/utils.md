# Utilities

## File related utilities

Several file-related utilities (`cp`, `ln`) recognize these enwars:

## SIMPLE_BACKUP_SUFFIX
Set backup suffix for files, or let the default `~` be used. 
By the way, to specify it on the command line use `--suffix` option.


## VERSION_CONTROL
The version control method may be selected via the `--backup` option or through
this environment variable.

Available values:
- `none`     or `off`    Never make backups (even if `--backup` is given).
- `numbered` or `t`      Make numbered backups.
- `existing` or `nil`    Numbered if numbered backups exist, simple otherwise.
- `simple`   or `never`  Always make simple backups.

As a special case, `cp` makes a backup of SOURCE when `--force` and `--backup` options are given and SOURCE and DEST are the same name for an existing, regular file.
