# less

Environment variables may be specified either in the system environment as usual, or in a `lesskey(1)` file. If environment variables are defined in more than one place, variables defined in a local lesskey file take precedence over variables defined in the system environment, which take precedence over variables defined in the system-wide lesskey file.

LESS specific: 
LESS 
LESSANSIMIDCHARS LESSANSIENDCHARS 
LESSBINFMT LESSUTFBINFMT 
LESSCHARDEF LESSCHARSET LESSMETACHARS LESSMETAESCAPE 
LESSOPEN LESSCLOSE 
LESSHISTFILE LESSHISTSIZE 
LESSKEY LESSKEYIN LESSKEY_SYSTEM LESSKEYIN_SYSTEM 
LESSECHO LESSEDIT LESSGLOBALTAGS LESSSECURE LESSSEPARATOR LESS_IS_MORE

Other: MORE COLUMNS LINES EDITOR VISUAL LANG LC_CTYPE PATH HOME SHELL TERM

## TOC

<!-- TOC -->

- [TOC](#toc)
- [LESS specific env vars](#less-specific-env-vars)
  - [LESS](#less)
  - [LESSANSIENDCHARS](#lessansiendchars)
  - [LESSANSIMIDCHARS](#lessansimidchars)
  - [LESSBINFMT](#lessbinfmt)
  - [LESSUTFBINFMT](#lessutfbinfmt)
  - [LESSCHARDEF](#lesschardef)
  - [LESSCHARSET](#lesscharset)
  - [LESSOPEN](#lessopen)
  - [LESSCLOSE](#lessclose)
  - [LESSECHO](#lessecho)
  - [LESSEDIT](#lessedit)
  - [LESSGLOBALTAGS](#lessglobaltags)
  - [LESSHISTFILE](#lesshistfile)
  - [LESSHISTSIZE](#lesshistsize)
  - [LESSKEYIN](#lesskeyin)
  - [LESSKEY](#lesskey)
  - [LESSKEYIN_SYSTEM](#lesskeyin_system)
  - [LESSKEY_SYSTEM](#lesskey_system)
  - [LESSMETACHARS](#lessmetachars)
  - [LESSMETAESCAPE](#lessmetaescape)
  - [LESSSECURE](#lesssecure)
  - [LESSSEPARATOR](#lessseparator)
  - [LESS_IS_MORE](#less_is_more)
- [Other env vars](#other-env-vars)
  - [MORE](#more)
  - [COLUMNS](#columns)
  - [LINES](#lines)
  - [EDITOR](#editor)
  - [VISUAL](#visual)
  - [LANG](#lang)
  - [LC_CTYPE](#lc_ctype)
  - [PATH](#path)
  - [HOME](#home)
  - [SHELL](#shell)
  - [TERM](#term)

<!-- /TOC -->

## LESS specific env vars

### LESS
Put options in this envar. The environment variable is parsed before the command line, so command line options override the LESS environment variable. If an option appears in the LESS variable, it can be reset to its default value on the command line by beginning the command line option with `-+`. Some options like `-k` or `-D` require a string to follow the option letter. The string for that option is considered to end when a dollar sign is found. For example, you can set two `-D` options like this: `LESS="Dn9.1$Ds4.1"`.

### LESSANSIENDCHARS
Characters which may end an ANSI color escape sequence (default "m").

### LESSANSIMIDCHARS
Characters which may appear between the ESC character and the end character in an ANSI color escape sequence (default `0123456789:;[?!"'#%()*+ `).


### LESSBINFMT
Format for displaying non-printable, non-control characters.

### LESSUTFBINFMT
Format for displaying non-printable Unicode code points.


### LESSCHARDEF
Defines a character set.

### LESSCHARSET
Selects a predefined character set.


### LESSOPEN
Command line to invoke the (optional) input-preprocessor.

### LESSCLOSE
Command line to invoke the (optional) input-postprocessor.


### LESSECHO
Name of the `lessecho` program (default `lessecho`). The `lessecho` program is needed to expand metacharacters, such as `*` and `?`, in filenames on Unix.

### LESSEDIT
Editor prototype string (used for the `v` command) (See PROMPTS).

### LESSGLOBALTAGS
Name of the command used by the `-t` option to find global tags. Normally should be set to "global" if your system has the `global(1)` command. If not set, global tags are not used.


### LESSHISTFILE
Name of the history file used to remember search commands and shell commands between invocations of less. If set to `-` or `/dev/null`, a history file is not used. The default is `$XDG_DATA_HOME/lesshst` or `$HOME/.lesshst`.

### LESSHISTSIZE
The maximum number of commands to save in the history file. The default is 100.

### LESSKEYIN
Name of the default lesskey source file.

### LESSKEY
Name of the default lesskey binary file. Not used if LESSKEYIN exists.

### LESSKEYIN_SYSTEM
Name of the default system-wide lesskey source file.

### LESSKEY_SYSTEM
Name of the default system-wide lesskey binary file. Not used if LESSKEYIN_SYSTEM exists.

### LESSMETACHARS
List of characters which are considered "metacharacters" by the shell.

### LESSMETAESCAPE
Prefix which less will add before each metacharacter in a command sent to the shell. If LESSMETAESCAPE is an empty string, commands containing metacharacters will not be passed to the shell.

### LESSSECURE
Runs less in "secure" mode (See SECURITY).

### LESSSEPARATOR
String to be appended to a directory name in filename completion.

### LESS_IS_MORE
Emulate the `more(1)` command.


## Other env vars

### MORE
Options which are passed to less automatically when running in more compatible mode.

### COLUMNS
Sets the number of columns on the screen. Takes precedence over the number of columns specified by the TERM variable. (But if you have a windowing system which supports TIOCGWINSZ or WIOCGETD, the window system's idea of the screen size takes precedence over the LINES and COLUMNS environment variables).

### LINES
Sets the number of lines on the screen. Takes precedence over the number of lines specified by the TERM variable. (But if you have a windowing system which supports TIOCGWINSZ or WIOCGETD, the window system's idea of the screen size takes precedence over the LINES and COLUMNS).

### EDITOR
The name of the editor (used for the `v` command).

### VISUAL
The name of the editor (used for the v command).

### LANG
Language for determining the character set.

### LC_CTYPE
Language for determining the character set.

### PATH
Search path (to find a lesskey file on MS-DOS and OS/2).

### HOME
User home directory is searched for lesskey file (on OS/2 searches INIT dir).

### SHELL
The shell used to execute the `!` command, as well as to expand filenames.

### TERM
The type of terminal on which less is being run.
