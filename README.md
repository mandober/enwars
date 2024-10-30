# Index of environment variables

List of environment variables (env vars, envars, enwars) on Linux.

<!-- TOC -->

- [BROWSER](#browser)
- [CDPATH](#cdpath)
- [CHILD_MAX](#child_max)
- [COLUMNS](#columns)
- [COMP_CWORD](#comp_cword)
- [COMP_LINE](#comp_line)
- [COMP_POINT](#comp_point)
- [COMP_TYPE](#comp_type)
- [COMP_KEY](#comp_key)
- [COMP_WORDBREAKS](#comp_wordbreaks)
- [COMP_WORDS](#comp_words)
- [COMPREPLY](#compreply)
- [COPROC](#coproc)
- [DIRSTACK](#dirstack)
- [DISPLAY](#display)
- [DOMAIN](#domain)
- [EDITOR](#editor)
- [EMACS](#emacs)
- [ENV](#env)
- [EUID](#euid)
- [EXECIGNORE](#execignore)
- [FCEDIT](#fcedit)
- [FIGNORE](#fignore)
- [FUNCNAME](#funcname)
- [FUNCNEST](#funcnest)
- [GLOBIGNORE](#globignore)
- [GROUPS](#groups)
- [histchars](#histchars)
- [HOME](#home)
- [HOSTALIASES](#hostaliases)
- [HISTCMD](#histcmd)
- [HISTCONTROL](#histcontrol)
- [HISTFILE](#histfile)
- [HISTFILESIZE](#histfilesize)
- [HISTIGNORE](#histignore)
- [HISTSIZE](#histsize)
- [HISTTIMEFORMAT](#histtimeformat)
- [HOSTFILE](#hostfile)
- [HOSTNAME](#hostname)
- [HOSTTYPE](#hosttype)
- [HTTP_PROXY](#http_proxy)
- [IFS](#ifs)
- [IGNOREEOF](#ignoreeof)
- [INPUTRC](#inputrc)
- [LANG](#lang)
- [LC_ALL](#lc_all)
- [LC_COLLATE](#lc_collate)
- [LC_CTYPE](#lc_ctype)
- [LC_MESSAGES](#lc_messages)
- [LC_NUMERIC](#lc_numeric)
- [LC_TIME](#lc_time)
- [LD_LIBRARY_PATH](#ld_library_path)
- [LINENO](#lineno)
- [LINES](#lines)
- [LOGNAME](#logname)
- [LPDEST](#lpdest)
- [LS_COLORS](#ls_colors)
- [MACHTYPE](#machtype)
- [MAIL](#mail)
- [MAILCHECK](#mailcheck)
- [MAILPATH](#mailpath)
- [MANPATH](#manpath)
- [MAPFILE](#mapfile)
- [NNTPSERVER](#nntpserver)
- [OLDPWD](#oldpwd)
- [OPTARG](#optarg)
- [OPTIND](#optind)
- [OPTERR](#opterr)
- [OSTYPE](#ostype)
- [PAGER](#pager)
- [PATH](#path)
- [PIPESTATUS](#pipestatus)
- [POSIXLY_CORRECT](#posixly_correct)
- [_POSIX2_VERSION](#_posix2_version)
- [PREFIX](#prefix)
- [PPID](#ppid)
- [PRINTER](#printer)
- [PROMPT_COMMAND](#prompt_command)
- [PROMPT_DIRTRIM](#prompt_dirtrim)
- [PS0](#ps0)
- [PS1](#ps1)
- [PS2](#ps2)
- [PS3](#ps3)
- [PS4](#ps4)
- [PWD](#pwd)
- [RANDOM](#random)
- [READLINE_LINE](#readline_line)
- [READLINE_POINT](#readline_point)
- [REPLY](#reply)
- [SECONDS](#seconds)
- [SHELL](#shell)
- [SHELLOPTS](#shellopts)
- [SHLVL](#shlvl)
- [SIMPLE_BACKUP_SUFFIX](#simple_backup_suffix)
- [TEMP](#temp)
- [TERM](#term)
- [TERM_PROGRAM](#term_program)
- [TERMCAP](#termcap)
- [TERMINFO](#terminfo)
- [TERMINFO_DIRS](#terminfo_dirs)
- [TMP](#tmp)
- [TMPDIR](#tmpdir)
- [TIMEFORMAT](#timeformat)
- [TMOUT](#tmout)
- [TMPDIR](#tmpdir-1)
- [TZ](#tz)
- [TZDIR](#tzdir)
- [UID](#uid)
- [USER](#user)
- [VISUAL](#visual)
- [VERSION_CONTROL](#version_control)
- [XDG_DATA_HOME](#xdg_data_home)
- [XDG_CONFIG_HOME](#xdg_config_home)
- [XDG_DATA_DIRS](#xdg_data_dirs)
- [XDG_CONFIG_DIRS](#xdg_config_dirs)
- [XDG_CACHE_HOME](#xdg_cache_home)
- [XDG_RUNTIME_DIR](#xdg_runtime_dir)
- [XENVIRONMENT](#xenvironment)
- [XFILESEARCHPATH](#xfilesearchpath)

<!-- /TOC -->



## BROWSER
Set path to default browser. If only name is set, uses PATH to search for it.

## CDPATH
A colon-separated list of dirs used like PATH but for dirs. Consulted by `cd`. User-settable env var.

If the target directory of the `cd` command is specified as a relative path name, the `cd` first searches for the target directory in cwd. If the target is not found, the path names that are listed in the CDPATH variable are searched consecutively until the target directory is found and the directory change is completed. If the target directory is not found, the current working directory is left unmodified. For example, if CDPATH is set to `/home/jean`, and there are home/jean/{bin,doc}. If cwd is `/home/jean/bin` typing `cd doc` changes cwd to `/home/jean/doc`.

- origin: bash
- value: colon-separated list of dirs
- read-by: cd
- access: user-settable
- purpose: navigation


## CHILD_MAX
Set the number of exited child status values for the shell to remember. Bash will not allow this value to be decreased below a POSIX-mandated minimum, and there is a maximum value (currently 8192) that this may not exceed. The minimum value is system-dependent.
> Shell: bash  

## COLUMNS
Used by the select command to determine the terminal width when printing selection lists. Automatically set if the checkwinsize option is enabled (see The Shopt Builtin), or in an interactive shell upon receipt of a SIGWINCH.

## COMP_CWORD
An index into ${COMP_WORDS} of the word containing the current cursor position. This variable is available only in shell functions invoked by the programmable completion facilities.
> Shell: bash, readline, completion

## COMP_LINE
The current command line. This variable is available only in shell functions and external commands invoked by the programmable completion facilities.
> Shell: bash, readline

## COMP_POINT
The index of the current cursor position relative to the beginning of the current command. If the current cursor position is at the end of the current command, the value of this variable is equal to ${#COMP_LINE}. This variable is available only in shell functions and external commands invoked by the programmable completion facilities.
> Shell: bash, readline

## COMP_TYPE
Set to an integer value corresponding to the type of completion attempted that caused a completion function to be called: TAB, for normal completion, '?', for listing completions after successive tabs, '!', for listing alternatives on partial word completion, '@', to list completions if the word is not unmodified, or '%', for menu completion. This variable is available only in shell functions and external commands invoked by the programmable completion facilities.
> Shell: bash, readline

## COMP_KEY
The key (or final key of a key sequence) used to invoke the current completion function.
> Shell: bash, readline

## COMP_WORDBREAKS
The set of characters that the Readline library treats as word separators when performing word completion. If COMP_WORDBREAKS is unset, it loses its special properties, even if it is subsequently reset.
> Shell: bash, readline

## COMP_WORDS
An array variable consisting of the individual words in the current command line. The line is split into words as Readline would split it, using COMP_WORDBREAKS as described above. This variable is available only in shell functions invoked by the programmable completion facilities.
> Shell: bash, readline

## COMPREPLY
An array variable from which Bash reads the possible completions generated by a shell function invoked by the programmable completion facility. Each array element contains one possible completion.
> Shell: bash, readline

## COPROC
An array variable created to hold the file descriptors for output from and input to an unnamed coprocess.

## DIRSTACK
An array variable containing the current contents of the directory stack. Directories appear in the stack in the order they are displayed by the dirs builtin. Assigning to members of this array variable may be used to modify directories already in the stack, but the pushd and popd builtins must be used to add and remove directories. Assignment to this variable will not change the current directory. If DIRSTACK is unset, it loses its special properties, even if it is subsequently reset.

## DISPLAY
Set X display name. `export DISPLAY=:0.1`

## DOMAIN
domain name

## EDITOR
Set name of default (line) text editor.

## EMACS
If Bash finds this variable in the environment when the shell starts with value 't', it assumes that the shell is running in an Emacs shell buffer and disables line editing.

## ENV
Similar to BASH_ENV; used when the shell is invoked in POSIX Mode.
> filename, sh, bash, sh hook

## EUID
The numeric effective user id of the current user. This variable is readonly.

## EXECIGNORE
*A colon-separated list of shell patterns* defining the list of filenames to be ignored by command search using PATH.

Files whose full pathnames match one of these patterns are not considered executable files for the purposes of completion and command execution via PATH lookup. This does not affect the behavior of the `[`, `test`, and `[[` commands. Full pathnames in the command hash table are not subject to EXECIGNORE. Use this variable to ignore shared library files that have the executable bit set, but are not executable files. The pattern matching honors the setting of the extglob shell option.

## FCEDIT
The editor used as a default by the -e option to the fc builtin command.

## FIGNORE
A colon-separated list of suffixes to ignore when performing filename completion. A filename whose suffix matches one of the entries in FIGNORE is excluded from the list of matched filenames. A sample value is '.o:~'

## FUNCNAME
An array variable containing the names of all shell functions currently in the execution call stack. The element with index 0 is the name of any currently-executing shell function. The bottom-most element (the one with the highest index) is "main". This variable exists only when a shell function is executing. Assignments to FUNCNAME have no effect. If FUNCNAME is unset, it loses its special properties, even if it is subsequently reset.

This variable can be used with BASH_LINENO and BASH_SOURCE. Each element of FUNCNAME has corresponding elements in BASH_LINENO and BASH_SOURCE to describe the call stack. For instance, ${FUNCNAME[$i]} was called from the file ${BASH_SOURCE[$i+1]} at line number ${BASH_LINENO[$i]}. The caller builtin displays the current call stack using this information.

## FUNCNEST
If set to a numeric value greater than 0, defines a maximum function nesting level. Function invocations that exceed this nesting level will cause the current command to abort.

## GLOBIGNORE
A colon-separated list of patterns defining the set of filenames to be ignored by filename expansion. If a filename matched by a filename expansion pattern also matches one of the patterns in GLOBIGNORE, it is removed from the list of matches. The pattern matching honors the setting of the extglob shell option.

## GROUPS
An array variable containing the list of groups of which the current user is a member. Assignments to GROUPS have no effect. If GROUPS is unset, it loses its special properties, even if it is subsequently reset.

## histchars
Up to three characters which control history expansion, quick substitution, and tokenization (see History Interaction). The first character is the history expansion character, that is, the character which signifies the start of a history expansion, normally '!'. The second character is the character which signifies 'quick substitution' when seen as the first character on a line, normally '^'. The optional third character is the character which indicates that the remainder of the line is a comment when found as the first character of a word, usually '#'. The history comment character causes history substitution to be skipped for the remaining words on the line. It does not necessarily cause the shell parser to treat the rest of the line as a comment.

## HOME
- $HOMEholds the current user's home directory
- auto set by `login(1)`, to the value taken from `passwd(4)` file
- dobles as default argument for `cd`
- old systems have used `LOGDIR` instead
- enwar_flavour: single directory name, as a string of course
- enwar_popularity: all-time fave, possibly no.1, always in top 5
- enwar_deference: revered by the lot
- enwar_necessity: high possibility of strange behavior. If unavailable at login, the user gets a tmp slum home hard-linked public toilet.


## HOSTALIASES
- gives the name of a file containing aliases to be used with `gethostbyname(3)`
- enwar_origin: 

## HISTCMD
- the history number, or index in the history list, of the current command.
- if unset, it loses its special properties, even if subsequently reset.
- enwar_precious: has special properties but may easily loose 'em for good
- enwar_precious: 


## HISTCONTROL
A colon-separated list of values controlling how commands are saved on the history list. If the list of values includes 'ignorespace', lines which begin with a space character are not saved in the history list. A value of 'ignoredups' causes lines which match the previous history entry to not be saved. A value of 'ignoreboth' is shorthand for 'ignorespace' and 'ignoredups'. A value of 'erasedups' causes all previous lines matching the current line to be removed from the history list before that line is saved. Any value not in the above list is ignored. If HISTCONTROL is unset, or does not include a valid value, all lines read by the shell parser are saved on the history list, subject to the value of HISTIGNORE. The second and subsequent lines of a multi-line compound command are not tested, and are added to the history regardless of the value of HISTCONTROL.

## HISTFILE
The name of the file to which the command history is saved. The default value is ~/.bash_history.

## HISTFILESIZE
The maximum number of lines contained in the history file. When this variable is assigned a value, the history file is truncated, if necessary, to contain no more than that number of lines by removing the oldest entries. The history file is also truncated to this size after writing it when a shell exits. If the value is 0, the history file is truncated to zero size. Non-numeric values and numeric values less than zero inhibit truncation. The shell sets the default value to the value of HISTSIZE after reading any startup files.
> bash

## HISTIGNORE
A colon-separated list of patterns used to decide which command lines should be saved on the history list. Each pattern is anchored at the beginning of the line and must match the complete line (no implicit '\*' is appended). Each pattern is tested against the line after the checks specified by HISTCONTROL are applied. In addition to the normal shell pattern matching characters, '&' matches the previous history line. '&' may be escaped using a backslash; the backslash is removed before attempting a match. The second and subsequent lines of a multi-line compound command are not tested, and are added to the history regardless of the value of HISTIGNORE. The pattern matching honors the setting of the extglob shell option. HISTIGNORE subsumes the function of HISTCONTROL. A pattern of '&' is identical to ignoredups, and a pattern of '[ ]*' is identical to ignorespace. Combining these two patterns, separating them with a colon, provides the functionality of ignoreboth.

## HISTSIZE
The maximum number of commands to remember on the history list. If the value is 0, commands are not saved in the history list. Numeric values less than zero result in every command being saved on the history list (there is no limit). The shell sets the default value to 500 after reading any startup files.
> bash

## HISTTIMEFORMAT
If this variable is set and not null, its value is used as a format string for strftime to print the time stamp associated with each history entry displayed by the history builtin. If this variable is set, time stamps are written to the history file so they may be preserved across shell sessions. This uses the history comment character to distinguish timestamps from other history lines.
> bash

## HOSTFILE
Contains the name of a file in the same format as /etc/hosts that should be read when the shell needs to complete a hostname. The list of possible hostname completions may be changed while the shell is running; the next time hostname completion is attempted after the value is changed, Bash adds the contents of the new file to the existing list. If HOSTFILE is set, but has no value, or does not name a readable file, Bash attempts to read /etc/hosts to obtain the list of possible hostname completions. When HOSTFILE is unset, the hostname list is cleared.
> bash

## HOSTNAME
The name of the current host.

## HOSTTYPE
A string describing the machine Bash is running on.
> bash

## HTTP_PROXY
This variable defnes which proxy server should be used for an Internet connection.

## IFS
List of characters that separate fields, when shell splits words as part of expansion.  
> bash

## IGNOREEOF
Controls the action of the shell on receipt of an EOF character as the sole input. If set, the value denotes the number of consecutive EOF characters that can be read as the first character on an input line before the shell will exit. If the variable exists but does not have a numeric value (or has no value) then the default is 10. If the variable does not exist, then EOF signifies the end of input to the shell. This is only in effect for interactive shells.
> bash

## INPUTRC
The name of the Readline initialization file, overriding the default of ~/.inputrc.
> readline

## LANG
Used to determine the locale category for any category not specifically selected with a variable starting with `LC_`.

## LC_ALL
This variable overrides the value of `LANG` and any other `LC_` variable specifying a locale category.

## LC_COLLATE
This variable determines the collation order used when sorting the results of filename expansion, and determines the behavior of range expressions, equivalence classes, and collating sequences within filename expansion and pattern matching.

## LC_CTYPE
This variable determines the interpretation of characters and the behavior of character 
classes within filename expansion and pattern matching.

## LC_MESSAGES
This variable determines the locale used to translate double-quoted strings preceded 
by a `$`.

## LC_NUMERIC
This variable determines the locale category used for number formatting.

## LC_TIME
determines the locale category used for data and time formatting.

## LD_LIBRARY_PATH
On many Unix systems with a dynamic linker, contains a colon-separated list of directories that the dynamic linker should search for shared objects when building a process image after exec, before searching in any other, default, directories. `LD_LIBRARY_PATH`, `LD_PRELOAD`, and other `LD_*` variables influence the behavior of the dynamic loader/linker.

## LINENO
The line number in the script or shell function currently executing.

## LINES
Used by the select command to determine the column length for printing selection lists. 
Automatically set if the checkwinsize option is enabled, or in an interactive shell upon 
receipt of a `SIGWINCH`.

## LOGNAME
The name of the logged-in user (used by some System-V derived programs). The default value of LOGNAME is automatically set by the login program to the user name that is specified in the passwd file. You should only need to refer to, not reset, this variable.

## LPDEST
PRINTER or LPDEST may specify the desired printer to use. See lpr(1).

## LS_COLORS
ls command's spec for colors

## MACHTYPE
A string that fully describes the system type on which Bash is executing, in the 
standard GNU cpu-company-system format.

## MAIL
If this parameter is set to a filename or directory name (and the MAILPATH variable is not set), Bash informs the user of the arrival of mail in the specified file or Maildir-format directory. Overridden by MAILPATH.  
This variable can be used to monitor any file or directory: 
- if file is monitored, the shell will print alerts when file's content is changed
- if directory is monitored, the shell will alert when new files are added or deleted from it
To monitor several files/directories and specify custom alert messages, see `MAILPATH`.  
Example: `MAIL=$HOME/.bashrc`  
> filename, hook

## MAILCHECK
Specifies how often (in seconds) the shell checks for mail (as specified in the MAILPATH or MAIL). The default is 60 seconds. When it is time to check for mail, the shell does so before displaying the primary prompt. If not set to an integer greater than 0, the shell disables mail checking.
> integer

## MAILPATH
A colon-separated list of filenames which the shell periodically checks for new mail.  
Each list entry can specify the message that is printed when new mail arrives in the mail file by separating the filename from the message with a `?`. When used in the text of the message, `$_` expands to the name of the current mail file (but it must be inside single quotes, otherwise it will expand into shell variable, `$_`, which contains the last argument of the previous command).  
This variable can be used to monitor any file or directory: see MAIL.  
Example: `MAILPATH=$HOME/.bashrc?'$_ modified!':$HOME/dots?'New file added in $_'`  
> filename and paths, hook

## MANPATH
Colon separated list of directories to search for manual pages.

## MAPFILE
An array variable created to hold the text read by the mapfile builtin when no variable name is supplied.

## NNTPSERVER
Specify a news server that some Usenet news readers require to access the news (nntp) server.

## OLDPWD
The previous working directory as set by the cd builtin.

## OPTARG
The value of the last option argument processed by the `getopts` builtin.

## OPTIND
The index of the last option argument processed by the `getopts` builtin.

## OPTERR
If set to the value 1, Bash displays error messages generated by the getopts builtin command.

## OSTYPE
A string describing the operating system Bash is running on.

## PAGER
Name of the program to be used for paging output. Default: `pager`

## PATH
The sequence of path prefixes that utilities apply in searching for an executable file known only by a filename.
- The prefixes are separated by a colon `:`.
- The prefixes need not have a trailing slash - when a non-zero-length prefix is applied to this filename, a slash is inserted between the prefix and the filename.
- A zero-length prefix indicates the current working directory. It appears as two adjacent colons `PATH=/bin::/sbin`, as an initial colon preceding the rest of the list `PATH=::/bin`, or as a trailing colon following the rest of the list `PATH=/bin::`. Putting CWD in PATH could present a security risk, especially if placed towards beginning of the value. A portable application must use an actual pathname, such as `.`, to represent the current working directory in PATH, e.g. `PATH=/bin:./node_modules/.bin`.
- The list is searched from beginning to end, applying the filename to each prefix, until an executable file with the specified name and appropriate execution permissions is found.
- If the pathname being sought contains a slash (relative pathname), the search through the PATH prefixes will not be performed as the specified path is resolved directly.
- If the pathname begins with a slash (absolute pathname), the specified path is resolved directly.
- If PATH is unset or is set to null, the path search is implementation-dependent.
- System-wide PATH is system-dependent, initially set as part of the login process and by the administrator. 
- Users can change PATH value; suitable files for persistant PATH and other environment variable settings that affect just a particular user are `~/.pam_environment` and `~/.profile`.
- Common default PATH value is `/usr/local/bin:/usr/local/sbin:/usr/bin:/usr/sbin:/bin:/sbin`.
[ **csp | common | user** ]  


## PIPESTATUS
An array variable (see Arrays) containing a list of exit status values from the processes in the most-recently-executed foreground pipeline (which may contain only a single command).


## POSIXLY_CORRECT
In a few cases, default behavior of the GNU utilities is incompatible with the POSIX standard. To suppress these incompatibilities, define this environment variable; unless you are checking for POSIX conformance, you probably don't need it.  

For example: normally, options and operands can appear in any order, and programs act as if all the options appear before any operands, e.g. `diff lao tzu -C 2` acts like `diff -C 2 lao tzu`, since `2` is an option-argument of `-C`. However, if POSIXLY_CORRECT is set, **options must appear before operands**, unless otherwise specified for a particular command.  

Newer versions of POSIX are occasionally incompatible with older versions. For example, older versions of POSIX allowed the command `diff -c -10` to have the same meaning as `diff -C 10`, but POSIX 1003.1-2001 `diff` no longer allows digit-string options like `-10`.  

[bash] If this variable is in the environment when bash starts, the shell enters POSIX mode before reading the startup files, as if the `bash --posix` invocation option had been supplied. If it is set while the shell is running, bash enables POSIX mode, as if the command `set -o posix` had been executed.  
<*`gnu`*> <*`bash`*> <*`user`*>

## _POSIX2_VERSION
The GNU utilities normally conform to the version of POSIX that is standard for your system. To cause them to conform to a different version of POSIX, define the `_POSIX2_VERSION` 
environment variable to a value of the form `YYYYMM` specifying the year and month the standard was adopted. Two values are currently supported: 199209 stands for **POSIX 1003.2-1992**, and 200112 stands for **POSIX 1003.1-2001**. For example, if you are running older software that assumes an older version of POSIX and uses `diff -c -10`, you can work around the compatibility problems by setting `_POSIX2_VERSION=199209` in your environment.

## PREFIX
Holds a root directory for new program installation. Usually `/usr/local`. It will 
contain a third-level file hierarchy under it (bin, etc, include, lib, sbin, share, src).
Many utilities will look up this variable upon installation to place their files there.

## PPID
[bash] The process ID of the shell's parent process. This variable is `read-only`.

## PRINTER
PRINTER or LPDEST may specify the desired printer to use. See lpr(1).

## PROMPT_COMMAND
If set, the value is interpreted as a command to execute before the printing of each primary prompt ($PS1).

## PROMPT_DIRTRIM
If set to a number greater than zero, the value is used as the number of trailing directory components to retain when expanding the \w and \W prompt string escapes (see Controlling the Prompt). Characters removed are replaced with an ellipsis.

## PS0
The value of this parameter is expanded like PS1 and displayed by interactive shells after reading a command and before the command is executed.

## PS1
The primary prompt string. The default value is `\s-\v\$`
*<sh>*

## PS2
The secondary prompt string. The default value is `>`
*<sh>*

## PS3
The value of this variable is used as the prompt for the select command. If this variable is not set, the select command prompts with '#? '

## PS4
The value is the prompt printed before the command line is echoed when the -x option is set (see The Set Builtin). The first character of PS4 is replicated multiple times, as necessary, to indicate multiple levels of indirection. The default is '+ '.

## PWD
This variable points to the current directory. Equivalent to the output of the command `pwd` when called without arguments. Changes to PWD are maintained by the `cd` command.

## RANDOM
Each time this parameter is referenced, a random integer between 0 and 32767 is generated. Assigning a value to this variable seeds the random number generator.

## READLINE_LINE
The contents of the Readline line buffer, for use with 'bind -x' (see Bash Builtins).

## READLINE_POINT
The position of the insertion point in the Readline line buffer, for use with 'bind -x' (see Bash Builtins).

## REPLY
The default variable for the read builtin.

## SECONDS
This variable expands to the number of seconds since the shell was started. Assignment to this variable resets the count to the value assigned, and the expanded value becomes the value assigned plus the number of seconds since the assignment.

## SHELL
The full pathname to the shell is kept in this environment variable. If it is not set when the shell starts, Bash assigns to it the full pathname of the current user's login shell.

## SHELLOPTS
A colon-separated list of enabled shell options. Each word in the list is a valid argument for `set -o` builtin. The options appearing in SHELLOPTS are those reported as enabled by `set -o`. If this variable is in the environment when Bash starts up, each shell option in the list will be enabled before reading any startup files. This variable is *readonly*.

## SHLVL
Incremented by one each time a new instance of Bash is started. This is intended to be a count of how deeply your Bash shells are nested.

## SIMPLE_BACKUP_SUFFIX
Some GNU programs (at least cp, install, ln, mv) can make backups of files before writing new versions. The option `--suffix=SUFFIX` specifies the SUFFIX to append to each backup file. If this option is not specified, the value of the `SIMPLE_BACKUP_SUFFIX` environment variable is used; if unset, the default is `~`.

## TEMP
Directory to store temporary files. See also TMP.

## TERM
Specifies the terminal model or family. Probably the most common value is 'xterm-256color'. This value says that the terminal is xterm compatible and supports 256 colors. You can check the associated entry with `infocmp $TERM`, which contains the string `colors#0x100` (0x100 is 256). There are actually numerous other entries with the 'xterm' prefix, like 'xterm-direct'. Doing `infocmp xterm-direct` shows `colors#0x1000000` and `pairs#0x10000`, which implies true color support (24-bit color, 2⁸×2⁸×2⁸ = 256³ = 2²⁴ = 16,777,216); `pairs` is the max numbers of color-pairs that can be displayed simultaneously (65,536).

*Terminfo* describes terminals by giving a set of capabilities which they have, by specifying how to perform screen operations, and by specifying padding requirements and initialization sequences. It is primarily used by screen-oriented programs. 

Setting this to an incompatible value may screw up different aspects (usually colors, but posibly other things too) of screen-programs.

This env var is related to the terminfo database of terminal escape codes. 

A utility that wants to emit special escape codes needs to lookup a proper sequence the current terminal supports. The terminfo maintains a database of terminal escape codes arranged by terminal names. So utilities usually read the TERM to get the terminal name, then search the terminfo database by that name.

## TERM_PROGRAM
Type of program used as a terminal. Similar to TERM.

## TERMCAP
The termcap (terminal capability) is an older standard, succeeded by 'terminfo', that associates concrete terminals with their characteristics. An entry in the termcap database lists terminal properties like number of supported colors, including all supported capabilities and their sequences. TERMCAP env var points to a custom termcap configuration.

## TERMINFO
Names a directory where an alternate terminfo database is stored. Use the TERMINFO variable in either the `/etc/profile` or `/etc/.login file`. For more information, see the terminfo(4) man page. When the TERMINFO environment variable is set, the system first checks the TERMINFO path defined by the user. If the system does not find a definition for a terminal in the TERMINFO directory defined by the user, it searches the default directory, `/usr/share/lib/terminfo`, for a definition. If the system does not find a definition in either location, the terminal is identified as "dumb".

## TERMINFO_DIRS
Directories searched for terminfo entries.

## TMP
Directory to store temporary files. Same as `TEMP`.

## TMPDIR
influences the path prefix of names created by `tempnam(3)` and other routines, and the temporary directory used by `sort(1)` and other programs.

## TIMEFORMAT
The value of this parameter is used as a format string specifying how the timing 
information for pipelines prefixed with the time reserved word should be displayed. 
The `%` character introduces an escape sequence that is expanded to a time value or other 
information. The escape sequences and their meanings are as follows; the braces denote 
optional portions.
```
%% = A literal '%'.
%[p][l]R = The elapsed time in seconds.
%[p][l]U = The number of CPU seconds spent in user mode.
%[p][l]S = The number of CPU seconds spent in system mode.
%P = The CPU percentage, computed as (%U + %S) / %R. 
```
The optional `p` is a digit specifying the precision, the number of fractional digits 
after a decimal point. A value of 0 causes no decimal point or fraction to be output. 
At most three places after the decimal point may be specified; values of `p` greater 
than 3 are changed to 3. If `p` is not specified, the value 3 is used. The optional `l` specifies a longer format, including minutes, of the form `MMmSS.FFs`. The value of `p` determines whether or not the fraction is included.If this variable is not set, Bash acts as if it had the value `$'\nreal\t%3lR\nuser\t%3lU\nsys\t%3lS'`. If the value is null, no timing information is displayed. A trailing newline is added when the format string is displayed.

## TMOUT
If set to a value greater than zero, TMOUT is treated as the default timeout for the `read` builtin. The `select` command terminates if input does not arrive after TMOUT seconds when input is coming from a terminal. In an interactive shell, the value is interpreted as the number of seconds to wait for a line of input after issuing the primary prompt. Bash terminates after waiting for that number of seconds if a complete line of input 
does not arrive.

## TMPDIR
If set, Bash uses its value as the name of a directory in which Bash creates temporary files for the shell's use.

## TZ
Sets the time zone. The time zone is used to display dates, for example, in the ls -l command. If TZ is not set in the user's environment, the system setting is used. Otherwise, Greenwich Mean Time is used. Commands that print times (and dates) use this variable to determine the time zone. If the TZ variable is left undefined, the operating system's current time zone setting is used. See timezone for details. On Windows, the MKS Toolkit makes use of the built-in timezone support, and you should not set the TZ environment variable.

## TZDIR
TZ and TZDIR give timezone information used by tzset(3) and through that by functions 
like ctime(3), localtime(3), mktime(3), strftime(3). See also tzselect(8).

## UID
Contains the numeric real user id of the current user. Commonly used in scripts, 
`[ $UID != 0 ] && echo "not root"`, to check whether the current script has been 
run as root user or regular user. This variable is readonly.  
`readonly`, `bash`, `zsh`

## USER
The name of the logged-in user (used by some BSD-derived programs).

## VISUAL
Set name of default (full-screen) text editor.

## VERSION_CONTROL
Some GNU programs (at least cp, install, ln, mv) can make backups of files before writing new versions. The option `--backup[=METHOD]` controls the type of backup to make. When this option is used but METHOD is not specified, the valujeof `VERSION_CONTROL` env var is used; if unset, the default backup type is 'existing'.

## XDG_DATA_HOME
defines the base directory relative to which user specific data files should be stored. If $XDG_DATA_HOME is either not set or empty, a default equal to $HOME/.local/share should be used.

## XDG_CONFIG_HOME
defines the base directory relative to which user specific configuration files should be stored. If $XDG_CONFIG_HOME is either not set or empty, a default equal to $HOME/.config should be used.

## XDG_DATA_DIRS
defines the preference-ordered set of base directories to search for data files in addition to the $XDG_DATA_HOME base directory. The directories in $XDG_DATA_DIRS should be seperated with a colon ':'.
If $XDG_DATA_DIRS is either not set or empty, a value equal to /usr/local/share/:/usr/share/ should be used.

## XDG_CONFIG_DIRS
defines the preference-ordered set of base directories to search for configuration files in addition to the $XDG_CONFIG_HOME base directory. The directories in $XDG_CONFIG_DIRS should be seperated with a colon ':'.
If $XDG_CONFIG_DIRS is either not set or empty, a value equal to /etc/xdg should be used.
The order of base directories denotes their importance; the first directory listed is the most important. When the same information is defined in multiple places the information defined relative to the more important base directory takes precedent. The base directory defined by $XDG_DATA_HOME is considered more important than any of the base directories defined by $XDG_DATA_DIRS. The base directory defined by $XDG_CONFIG_HOME is considered more important than any of the base directories defined by $XDG_CONFIG_DIRS.

## XDG_CACHE_HOME
defines the base directory relative to which user specific non-essential data files should be stored. If $XDG_CACHE_HOME is either not set or empty, a default equal to $HOME/.cache should be used.

## XDG_RUNTIME_DIR
defines the base directory relative to which user-specific non-essential runtime files and other file objects (such as sockets, named pipes, ...) should be stored. The directory MUST be owned by the user, and he MUST be the only one having read and write access to it. Its Unix access mode MUST be 0700.
The lifetime of the directory MUST be bound to the user being logged in. It MUST be created when the user first logs in and if the user fully logs out the directory MUST be removed. If the user logs in more than once he should get pointed to the same directory, and it is mandatory that the directory continues to exist from his first login to his last logout on the system, and not removed in between. Files in the directory MUST not survive reboot or a full logout/login cycle.
The directory MUST be on a local file system and not shared with any other system. The directory MUST by fully-featured by the standards of the operating system. More specifically, on Unix-like operating systems AF_UNIX sockets, symbolic links, hard links, proper permissions, file locking, sparse files, memory mapping, file change notifications, a reliable hard link count must be supported, and no restrictions on the file name character set should be imposed. Files in this directory MAY be subjected to periodic clean-up. To ensure that your files are not removed, they should have their access time timestamp modified at least once every 6 hours of monotonic time or the 'sticky' bit should be set on the file.
If $XDG_RUNTIME_DIR is not set applications should fall back to a replacement directory with similar capabilities and print a warning message. Applications should use this directory for communication and synchronization purposes and should not place larger files in it, since it might reside in runtime memory and cannot necessarily be swapped out to disk.

## XENVIRONMENT
location of your personal settings for X behavior

## XFILESEARCHPATH
paths to search for graphical libraries

---

`special` attribute means that if varible is unset, it loses its special properties, even if it is subsequently reset.  
