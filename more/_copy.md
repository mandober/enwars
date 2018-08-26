# Environment variables

Environment variables provide a way to influence the behaviour of software on the system. The values of environment variables are local, which means they are specific to the running process in or for which they were set.


## TOC

<!-- TOC -->

- [Environment variables](#environment-variables)
  - [TOC](#toc)
  - [Common variables](#common-variables)
    - [HOME](#home)
    - [USER](#user)
    - [LOGNAME](#logname)
    - [PATH](#path)
    - [TMPDIR](#tmpdir)
    - [PWD](#pwd)
    - [LD_LIBRARY_PATH](#ld_library_path)
    - [CDPATH](#cdpath)
    - [IFS](#ifs)
    - [MAIL](#mail)
    - [MAILPATH](#mailpath)
    - [OPTARG](#optarg)
    - [OPTIND](#optind)
    - [PS1](#ps1)
    - [PS2](#ps2)
    - [COLUMNS](#columns)
  - [Bash variables](#bash-variables)
    - [BASH](#bash)
    - [BASHOPTS](#bashopts)
    - [BASHPID](#bashpid)
    - [BASH_ALIASES](#bash_aliases)
    - [BASH_ARGC](#bash_argc)
    - [BASH_ARGV](#bash_argv)
    - [BASH_CMDS](#bash_cmds)
    - [BASH_COMMAND](#bash_command)
    - [BASH_COMPAT](#bash_compat)
    - [BASH_ENV](#bash_env)
    - [BASH_EXECUTION_STRING](#bash_execution_string)
    - [BASH_LINENO](#bash_lineno)
    - [BASH_LOADABLES_PATH](#bash_loadables_path)
    - [BASH_REMATCH](#bash_rematch)
    - [BASH_SOURCE](#bash_source)
    - [BASH_SUBSHELL](#bash_subshell)
    - [BASH_VERSINFO](#bash_versinfo)
    - [BASH_VERSINFO](#bash_versinfo-1)
    - [BASH_VERSION](#bash_version)
    - [BASH_XTRACEFD](#bash_xtracefd)
    - [CHILD_MAX](#child_max)
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
    - [IGNOREEOF](#ignoreeof)
    - [INPUTRC](#inputrc)
    - [LANG](#lang)
    - [LC_ALL](#lc_all)
    - [LC_COLLATE](#lc_collate)
    - [LC_CTYPE](#lc_ctype)
    - [LC_MESSAGES](#lc_messages)
    - [LC_NUMERIC](#lc_numeric)
    - [LC_TIME](#lc_time)
    - [LINENO](#lineno)
    - [LINES](#lines)
    - [MACHTYPE](#machtype)
    - [MAILCHECK](#mailcheck)
    - [MAPFILE](#mapfile)
    - [OLDPWD](#oldpwd)
    - [OPTERR](#opterr)
    - [OSTYPE](#ostype)
    - [PIPESTATUS](#pipestatus)
    - [POSIXLY_CORRECT](#posixly_correct)
    - [PPID](#ppid)
    - [PROMPT_COMMAND](#prompt_command)
    - [PROMPT_DIRTRIM](#prompt_dirtrim)
    - [PS0](#ps0)
    - [PS3](#ps3)
    - [PS4](#ps4)
    - [RANDOM](#random)
    - [READLINE_LINE](#readline_line)
    - [READLINE_POINT](#readline_point)
    - [REPLY](#reply)
    - [SECONDS](#seconds)
    - [SHELL](#shell)
    - [SHELLOPTS](#shellopts)
    - [SHLVL](#shlvl)
    - [TIMEFORMAT](#timeformat)
    - [TMOUT](#tmout)
    - [TMPDIR](#tmpdir-1)
    - [UID](#uid)
  - [Other, commonly used variables](#other-commonly-used-variables)
    - [TZ](#tz)
    - [TZDIR](#tzdir)
    - [PRINTER](#printer)
    - [LPDEST](#lpdest)
    - [TERM](#term)
    - [TERMINFO](#terminfo)
    - [TERMCAP](#termcap)
    - [LOGNAME](#logname-1)
    - [MANPATH](#manpath)
    - [EDITOR](#editor)
    - [VISUAL](#visual)
    - [BROWSER](#browser)
    - [PAGER](#pager)
    - [DISPLAY](#display)
    - [LS_COLORS](#ls_colors)
    - [DOMAIN](#domain)
    - [HOSTALIASES](#hostaliases)
    - [XENVIRONMENT](#xenvironment)
    - [XFILESEARCHPATH](#xfilesearchpath)
  - [XDG Base Directory Specification](#xdg-base-directory-specification)
    - [XDG_DATA_HOME](#xdg_data_home)
    - [XDG_CONFIG_HOME](#xdg_config_home)
    - [XDG_DATA_DIRS](#xdg_data_dirs)
    - [XDG_CONFIG_DIRS](#xdg_config_dirs)
    - [XDG_CACHE_HOME](#xdg_cache_home)
    - [XDG_RUNTIME_DIR](#xdg_runtime_dir)
  - [Locale](#locale)
  - [Application-specific environment variables](#application-specific-environment-variables)

<!-- /TOC -->




Environment variables recognized by Bourne shell: [PATH](#path), [CDPATH](#cdpath), [HOME](#home), [IFS](#ifs), [MAIL](#mail), [MAILPATH](#mailpath), [OPTARG](#optarg), [OPTIND](#optind), [PS1](#ps1), [PS2](#ps2)  


---
`common` - common variable
`sh` - Bourne shell variable  
`dash` - dash shell variable  
`bash` - bash variable  
`zsh` - zsh variable  

`dir` - single path  
`csp` - colon-separated paths  
`iarr` - indexed array  
`aarr` - associative array  
`chr` - list of characters  
`ro` - read-only  
`user` - user-settable  
`sys` - set by the system  
`spec` - special: if unset, it loses its special properties  


---


## Common variables

There are quite a few common, well-known environment variables for which the meaning and the format have been agreed upon and they are used by many applications.



### HOME
The current user's home directory. Set automatically by `login(1)` from the user's login directory in the password file `passwd(4)`. This environment variable also functions as the default argument for the `cd` builtin.  
[ **dir** ]


### USER
The name of the logged-in user (used by some BSD-derived programs).


### LOGNAME
The name of the logged-in user (used by some System-V derived programs).


### PATH
The sequence of path prefixes that certain functions and utilities apply in searching for an executable file known only by a filename.

- The prefixes are separated by a colon `:`.
- The prefixes need not have a trailing slash - when a non-zero-length prefix is applied to this filename, a slash is inserted between the prefix and the filename.
- A zero-length prefix indicates the current working directory (CWD). It appears as two adjacent colons `PATH=/bin::/sbin`, as an initial colon preceding the rest of the list `PATH=::/bin`, or as a trailing colon following the rest of the list `PATH=/bin::`. Putting CWD in PATH could present a security risk, especially if placed towards beginning of the value. A portable application must use an actual pathname, such as `.`, to represent the current working directory in PATH, e.g. `PATH=/bin:./node_modules/.bin`.
- The list is searched from beginning to end, applying the filename to each prefix, until an executable file with the specified name and appropriate execution permissions is found.
- If the pathname being sought contains a slash (relative pathname), the search through the PATH prefixes will not be performed as the specified path is resolved directly.
- If the pathname begins with a slash (absolute pathname), the specified path is resolved directly.
- If PATH is unset or is set to null, the path search is implementation-dependent.
- System-wide PATH is system-dependent, initially set as part of the login process and by the administrator. 
- Users can change PATH value; suitable files for persistant PATH and other environment variable settings that affect just a particular user are `~/.pam_environment` and `~/.profile`.
- Common default PATH value is `/usr/local/bin:/usr/local/sbin:/usr/bin:/usr/sbin:/bin:/sbin`.

[ **csp | common | user** ]  



### TMPDIR
influences the path prefix of names created by `tempnam(3)` and other routines, and the temporary directory used by `sort(1)` and other programs.



### PWD
This variable points to the current directory. Equivalent to the output of the command `pwd` when called without arguments. Changes to PWD are maintained by the `cd` command.


### LD_LIBRARY_PATH

On many Unix systems with a dynamic linker, contains a colon-separated list of directories that the dynamic linker should search for shared objects when building a process image after exec, before searching in any other, default, directories. `LD_LIBRARY_PATH`, `LD_PRELOAD`, and other `LD_*` variables influence the behavior of the dynamic loader/linker.




### CDPATH
A colon-separated list of directories used as a search path for the `cd` builtin command. This user-settable variable is used to specify frequently visited directories.
- If the target directory of the `cd` command is specified as a relative path name, the `cd` first searches for the target directory in the current directory `.`.
- If the target is not found, the path names that are listed in the CDPATH variable are searched consecutively until the target directory is found and the directory change is completed.
- If the target directory is not found, the current working directory is left unmodified.
- For example, suppose the CDPATH variable is set to `/home/jean`, and two directories exist under `/home/jean`, `bin`, and `doc`. If you are in the `/home/jean/bin` directory and type `cd doc`, you change directories to `/home/jean/doc`, even though you do not specify a full path.  

[ **csp | common | user** ]  

type   |  sh  | bash | zsh
-------|------|------|----
paths  |  ✓   |  ✓   | ✓
phs    |      |     | ✓


### IFS
List of characters that separate fields, when shell splits words as part of expansion.  
[`c`]  



### MAIL
If this parameter is set to a filename or directory name (and the MAILPATH variable is not set), Bash informs the user of the arrival of mail in the specified file or Maildir-format directory. Overridden by MAILPATH.
- if filename is specified, bash will monitor that file for changes
- if directory is specified, bash will dislay alert when new file is added to that directory.
- To monitor several files or directories and specify custom messages, see `MAILPATH`.
[`p`]  



### MAILPATH
A colon-separated list of filenames which the shell periodically checks for new mail. Each list entry can specify the message that is printed when new mail arrives in the mail file by separating the filename from the message with a `?`. When used in the text of the message, `$_` expands to the name of the current mail file. There is a maximum of 10 mailboxes that can be monitored at once (`dash`).
*<sh>*


### OPTARG
The value of the last option argument processed by the `getopts` builtin.
*<sh>*


### OPTIND
The index of the last option argument processed by the `getopts` builtin.
 *<sh>*


### PS1
The primary prompt string. The default value is `\s-\v\$`
*<sh>*

### PS2
The secondary prompt string. The default value is `>`
*<sh>*


### COLUMNS
Used by the select command to determine the terminal width when printing selection lists. Automatically set if the checkwinsize option is enabled (see The Shopt Builtin), or in an interactive shell upon receipt of a SIGWINCH.




## Bash variables

Bash uses certain shell variables in the same way as the Bourne shell. In some cases, Bash assigns a default value to the variable. These variables are set or used by Bash, but other shells do not normally treat them specially.


### BASH
The full pathname used to execute the current instance of Bash.



### BASHOPTS
A colon-separated list of enabled shell options. Each word in the list is a valid arg
for `shopt -s`. The options appearing in BASHOPTS are those reported as `on` by `shopt`.
If this variable is in the environment when Bash starts up, each shell option in the 
list will be enabled before reading any startup files. This variable is *readonly*.



### BASHPID
Expands to the process ID of the current Bash process. This differs from `$$` under 
certain circumstances, such as subshells that do not require Bash to be re-initialized.



### BASH_ALIASES
An associative array variable whose members correspond to the internal list of aliases 
as maintained by the alias builtin. Elements added to this array appear in the alias list;
however, unsetting array elements currently does not cause aliases to be removed from the
alias list. *If unset, it loses its special properties*, even if it is subsequently reset.



### BASH_ARGC
An array variable whose values are the number of parameters in each frame of the current 
bash execution call stack. The number of parameters to the current subroutine (shell 
function or script executed with `source`) is at the top of the stack. When a subroutine 
is executed, the number of parameters passed is pushed onto BASH_ARGC. The shell sets 
BASH_ARGC only when in extended debugging mode, `shopt -s extdebug`.

### BASH_ARGV
An array variable containing all of the parameters in the current bash execution call 
stack. The final parameter of the last subroutine call is at the top of the stack; the 
first parameter of the initial call is at the bottom. When a subroutine is executed, the 
parameters supplied are pushed onto BASH_ARGV. The shell sets BASH_ARGV only when in 
extended debugging mode, `shopt -s extdebug`.

### BASH_CMDS
An associative array variable whose members correspond to the internal hash table of 
commands as maintained by the `hash` builtin. Elements added to this array appear in the 
hash table; however, unsetting array elements currently does not cause command names to 
be removed from the hash table. *If unset, it loses its special properties*, even if it 
is subsequently reset.



### BASH_COMMAND
The command currently being executed or about to be executed, unless the shell is 
executing a command as the result of a trap, in which case it is the command executing 
at the time of the trap.



### BASH_COMPAT
The value is used to set the shell’s compatibility level. See The Shopt Builtin, for a 
description of the various compatibility levels and their effects. The value may be a 
decimal number (e.g., 4.2) or an integer (e.g., 42) corresponding to the desired 
compatibility level. If BASH_COMPAT is unset or set to the empty string, the compatibility 
level is set to the default for the current version. If BASH_COMPAT is set to a value 
that is not one of the valid compatibility levels, the shell prints an error message and 
sets the compatibility level to the default for the current version. The valid compatibility 
levels correspond to the compatibility options accepted by the `shopt` builtin (for 
example, compat42 means that 4.2 and 42 are valid values). The current version is also 
a valid value.



### BASH_ENV
If this variable is set when Bash is invoked to execute a shell script, its value is 
expanded and used as the name of a startup file to read before executing the script.



### BASH_EXECUTION_STRING
The command argument to the -c invocation option.



### BASH_LINENO
An array variable whose members are the line numbers in source files where each corresponding member of FUNCNAME was invoked. ${BASH_LINENO[$i]} is the line number in the source file (${BASH_SOURCE[$i+1]}) where ${FUNCNAME[$i]} was called (or ${BASH_LINENO[$i-1]} if referenced within another shell function). Use LINENO to obtain the current line number.



### BASH_LOADABLES_PATH
A colon-separated list of directories in which the shell looks for dynamically loadable builtins specified by the enable command.



### BASH_REMATCH
An array variable whose members are assigned by the ‘=~’ binary operator to the [[ conditional 
command. The element with index 0 is the portion of the string matching the entire 
regular expression. The element with index n is the portion of the string matching the 
nth parenthesized subexpression. This variable is READ-ONLY.



### BASH_SOURCE
An array variable whose members are the source filenames where the corresponding shell function names in the FUNCNAME array variable are defined. The shell function ${FUNCNAME[$i]} is defined in the file ${BASH\_SOURCE[$i]} and called from ${BASH_SOURCE[$i+1]}



### BASH_SUBSHELL
Incremented by one within each subshell or subshell environment when the shell begins executing in that environment. The initial value is 0.



### BASH_VERSINFO
A readonly array variable (see Arrays) whose members hold version information for this instance of Bash. The values assigned to the array members are as follows:


### BASH_VERSINFO
BASH_VERSINFO[0] - The major version number (the release).  
BASH_VERSINFO[1] - The minor version number (the version).  
BASH_VERSINFO[2] - The patch level.  
BASH_VERSINFO[3] - The build version.  
BASH_VERSINFO[4] - The release status (e.g., beta1).
BASH_VERSINFO[5] - The value of MACHTYPE.  



### BASH_VERSION
The version number of the current instance of Bash.



### BASH_XTRACEFD

If set to an integer corresponding to a valid file descriptor, Bash will write the trace output generated when ‘set -x’ is enabled to that file descriptor. This allows tracing output to be separated from diagnostic and error messages. The file descriptor is closed when BASH\_XTRACEFD is unset or assigned a new value. Unsetting BASH\_XTRACEFD or assigning it the empty string causes the trace output to be sent to the standard error. Note that setting BASH_XTRACEFD to 2 (the standard error file descriptor) and then unsetting it will result in the standard error being closed.



### CHILD_MAX
Set the number of exited child status values for the shell to remember. Bash will not allow this value to be decreased below a POSIX-mandated minimum, and there is a maximum value (currently 8192) that this may not exceed. The minimum value is system-dependent.




### COMP_CWORD
An index into ${COMP_WORDS} of the word containing the current cursor position. This variable is available only in shell functions invoked by the programmable completion facilities (see Programmable Completion).



### COMP_LINE
The current command line. This variable is available only in shell functions and external commands invoked by the programmable completion facilities (see Programmable Completion).



### COMP_POINT
The index of the current cursor position relative to the beginning of the current command. If the current cursor position is at the end of the current command, the value of this variable is equal to ${#COMP_LINE}. This variable is available only in shell functions and external commands invoked by the programmable completion facilities (see Programmable Completion).



### COMP_TYPE
Set to an integer value corresponding to the type of completion attempted that caused a completion function to be called: TAB, for normal completion, ‘?’, for listing completions after successive tabs, ‘!’, for listing alternatives on partial word completion, ‘@’, to list completions if the word is not unmodified, or ‘%’, for menu completion. This variable is available only in shell functions and external commands invoked by the programmable completion facilities (see Programmable Completion).



### COMP_KEY
The key (or final key of a key sequence) used to invoke the current completion function.



### COMP_WORDBREAKS
The set of characters that the Readline library treats as word separators when performing word completion. If COMP_WORDBREAKS is unset, it loses its special properties, even if it is subsequently reset.



### COMP_WORDS
An array variable consisting of the individual words in the current command line. The line is split into words as Readline would split it, using COMP_WORDBREAKS as described above. This variable is available only in shell functions invoked by the programmable completion facilities.


### COMPREPLY
An array variable from which Bash reads the possible completions generated by a shell function invoked by the programmable completion facility. Each array element contains one possible completion.


### COPROC
An array variable created to hold the file descriptors for output from and input to an unnamed coprocess.



### DIRSTACK
An array variable containing the current contents of the directory stack. Directories appear in the stack in the order they are displayed by the dirs builtin. Assigning to members of this array variable may be used to modify directories already in the stack, but the pushd and popd builtins must be used to add and remove directories. Assignment to this variable will not change the current directory. If DIRSTACK is unset, it loses its special properties, even if it is subsequently reset.



### EMACS
If Bash finds this variable in the environment when the shell starts with value ‘t’, it assumes that the shell is running in an Emacs shell buffer and disables line editing.



### ENV
Similar to BASH_ENV; used when the shell is invoked in POSIX Mode.



### EUID
The numeric effective user id of the current user. This variable is readonly.



### EXECIGNORE
A colon-separated list of shell patterns defining the list of filenames to be ignored by command search using PATH. Files whose full pathnames match one of these patterns are not considered executable files for the purposes of completion and command execution via PATH lookup. This does not affect the behavior of the \[, test, and [[ commands. Full pathnames in the command hash table are not subject to EXECIGNORE. Use this variable to ignore shared library files that have the executable bit set, but are not executable files. The pattern matching honors the setting of the extglob shell option.



### FCEDIT
The editor used as a default by the -e option to the fc builtin command.



### FIGNORE
A colon-separated list of suffixes to ignore when performing filename completion. A filename whose suffix matches one of the entries in FIGNORE is excluded from the list of matched filenames. A sample value is ‘.o:~’



### FUNCNAME
An array variable containing the names of all shell functions currently in the execution call stack. The element with index 0 is the name of any currently-executing shell function. The bottom-most element (the one with the highest index) is "main". This variable exists only when a shell function is executing. Assignments to FUNCNAME have no effect. If FUNCNAME is unset, it loses its special properties, even if it is subsequently reset.

This variable can be used with BASH_LINENO and BASH_SOURCE. Each element of FUNCNAME has corresponding elements in BASH_LINENO and BASH_SOURCE to describe the call stack. For instance, ${FUNCNAME[$i]} was called from the file ${BASH_SOURCE[$i+1]} at line number ${BASH_LINENO[$i]}. The caller builtin displays the current call stack using this information.



### FUNCNEST
If set to a numeric value greater than 0, defines a maximum function nesting level. Function invocations that exceed this nesting level will cause the current command to abort.



### GLOBIGNORE
A colon-separated list of patterns defining the set of filenames to be ignored by filename expansion. If a filename matched by a filename expansion pattern also matches one of the patterns in GLOBIGNORE, it is removed from the list of matches. The pattern matching honors the setting of the extglob shell option.



### GROUPS
An array variable containing the list of groups of which the current user is a member. Assignments to GROUPS have no effect. If GROUPS is unset, it loses its special properties, even if it is subsequently reset.



### histchars
Up to three characters which control history expansion, quick substitution, and tokenization (see History Interaction). The first character is the history expansion character, that is, the character which signifies the start of a history expansion, normally ‘!’. The second character is the character which signifies ‘quick substitution’ when seen as the first character on a line, normally ‘^’. The optional third character is the character which indicates that the remainder of the line is a comment when found as the first character of a word, usually ‘#’. The history comment character causes history substitution to be skipped for the remaining words on the line. It does not necessarily cause the shell parser to treat the rest of the line as a comment.


### HISTCMD
The history number, or index in the history list, of the current command. If HISTCMD is unset, it loses its special properties, even if it is subsequently reset.


### HISTCONTROL
A colon-separated list of values controlling how commands are saved on the history list. If the list of values includes ‘ignorespace’, lines which begin with a space character are not saved in the history list. A value of ‘ignoredups’ causes lines which match the previous history entry to not be saved. A value of ‘ignoreboth’ is shorthand for ‘ignorespace’ and ‘ignoredups’. A value of ‘erasedups’ causes all previous lines matching the current line to be removed from the history list before that line is saved. Any value not in the above list is ignored. If HISTCONTROL is unset, or does not include a valid value, all lines read by the shell parser are saved on the history list, subject to the value of HISTIGNORE. The second and subsequent lines of a multi-line compound command are not tested, and are added to the history regardless of the value of HISTCONTROL.


### HISTFILE
The name of the file to which the command history is saved. The default value is ~/.bash_history.


### HISTFILESIZE
The maximum number of lines contained in the history file. When this variable is assigned a value, the history file is truncated, if necessary, to contain no more than that number of lines by removing the oldest entries. The history file is also truncated to this size after writing it when a shell exits. If the value is 0, the history file is truncated to zero size. Non-numeric values and numeric values less than zero inhibit truncation. The shell sets the default value to the value of HISTSIZE after reading any startup files.


### HISTIGNORE
A colon-separated list of patterns used to decide which command lines should be saved on the history list. Each pattern is anchored at the beginning of the line and must match the complete line (no implicit ‘\*’ is appended). Each pattern is tested against the line after the checks specified by HISTCONTROL are applied. In addition to the normal shell pattern matching characters, ‘&’ matches the previous history line. ‘&’ may be escaped using a backslash; the backslash is removed before attempting a match. The second and subsequent lines of a multi-line compound command are not tested, and are added to the history regardless of the value of HISTIGNORE. The pattern matching honors the setting of the extglob shell option. HISTIGNORE subsumes the function of HISTCONTROL. A pattern of ‘&’ is identical to ignoredups, and a pattern of ‘[ ]*’ is identical to ignorespace. Combining these two patterns, separating them with a colon, provides the functionality of ignoreboth.



### HISTSIZE
The maximum number of commands to remember on the history list. If the value is 0, commands are not saved in the history list. Numeric values less than zero result in every command being saved on the history list (there is no limit). The shell sets the default value to 500 after reading any startup files.



### HISTTIMEFORMAT
If this variable is set and not null, its value is used as a format string for strftime to print the time stamp associated with each history entry displayed by the history builtin. If this variable is set, time stamps are written to the history file so they may be preserved across shell sessions. This uses the history comment character to distinguish timestamps from other history lines.



### HOSTFILE
Contains the name of a file in the same format as /etc/hosts that should be read when the shell needs to complete a hostname. The list of possible hostname completions may be changed while the shell is running; the next time hostname completion is attempted after the value is changed, Bash adds the contents of the new file to the existing list. If HOSTFILE is set, but has no value, or does not name a readable file, Bash attempts to read /etc/hosts to obtain the list of possible hostname completions. When HOSTFILE is unset, the hostname list is cleared.



### HOSTNAME
The name of the current host.



### HOSTTYPE
A string describing the machine Bash is running on.



### IGNOREEOF
Controls the action of the shell on receipt of an EOF character as the sole input. If set, the value denotes the number of consecutive EOF characters that can be read as the first character on an input line before the shell will exit. If the variable exists but does not have a numeric value (or has no value) then the default is 10. If the variable does not exist, then EOF signifies the end of input to the shell. This is only in effect for interactive shells.



### INPUTRC
The name of the Readline initialization file, overriding the default of ~/.inputrc.



### LANG
Used to determine the locale category for any category not specifically selected with a 
variable starting with `LC_`.



### LC_ALL
This variable overrides the value of `LANG` and any other `LC_` variable specifying a 
locale category.


### LC_COLLATE
This variable determines the collation order used when sorting the results of filename 
expansion, and determines the behavior of range expressions, equivalence classes, and 
collating sequences within filename expansion and pattern matching.



### LC_CTYPE
This variable determines the interpretation of characters and the behavior of character 
classes within filename expansion and pattern matching.



### LC_MESSAGES
This variable determines the locale used to translate double-quoted strings preceded 
by a `$`.



### LC_NUMERIC
This variable determines the locale category used for number formatting.


### LC_TIME
determines the locale category used for data and time formatting.



### LINENO
The line number in the script or shell function currently executing.

### LINES
Used by the select command to determine the column length for printing selection lists. 
Automatically set if the checkwinsize option is enabled, or in an interactive shell upon 
receipt of a `SIGWINCH`.



### MACHTYPE
A string that fully describes the system type on which Bash is executing, in the 
standard GNU cpu-company-system format.



### MAILCHECK
How often (in seconds) that the shell should check for mail in the files specified in the MAILPATH or MAIL variables. The default is 60 seconds. When it is time to check for mail, the shell does so before displaying the primary prompt. If this variable is unset, or set to a value that is not a number greater than or equal to zero, the shell disables mail checking.


### MAPFILE
An array variable created to hold the text read by the mapfile builtin when no variable name is supplied.


### OLDPWD
The previous working directory as set by the cd builtin.



### OPTERR
If set to the value 1, Bash displays error messages generated by the getopts builtin command.



### OSTYPE
A string describing the operating system Bash is running on.



### PIPESTATUS
An array variable (see Arrays) containing a list of exit status values from the processes in the most-recently-executed foreground pipeline (which may contain only a single command).



### POSIXLY_CORRECT
If this variable is in the environment when Bash starts, the shell enters POSIX mode 
before reading the startup files, as if the `bash --posix` invocation option had been 
supplied. If it is set while the shell is running, Bash enables POSIX mode, as if the 
command `set -o posix` had been executed.   



### PPID
The process ID of the shell’s parent process. This variable is readonly.



### PROMPT_COMMAND
If set, the value is interpreted as a command to execute before the printing of each primary prompt ($PS1).



### PROMPT_DIRTRIM
If set to a number greater than zero, the value is used as the number of trailing directory components to retain when expanding the \w and \W prompt string escapes (see Controlling the Prompt). Characters removed are replaced with an ellipsis.



### PS0
The value of this parameter is expanded like PS1 and displayed by interactive shells after reading a command and before the command is executed.



### PS3
The value of this variable is used as the prompt for the select command. If this variable is not set, the select command prompts with ‘#? ’



### PS4
The value is the prompt printed before the command line is echoed when the -x option is set (see The Set Builtin). The first character of PS4 is replicated multiple times, as necessary, to indicate multiple levels of indirection. The default is ‘+ ’.



### RANDOM
Each time this parameter is referenced, a random integer between 0 and 32767 is generated. Assigning a value to this variable seeds the random number generator.



### READLINE_LINE
The contents of the Readline line buffer, for use with ‘bind -x’ (see Bash Builtins).



### READLINE_POINT
The position of the insertion point in the Readline line buffer, for use with ‘bind -x’ (see Bash Builtins).



### REPLY
The default variable for the read builtin.



### SECONDS
This variable expands to the number of seconds since the shell was started. Assignment to this variable resets the count to the value assigned, and the expanded value becomes the value assigned plus the number of seconds since the assignment.



### SHELL
The full pathname to the shell is kept in this environment variable. If it is not set 
when the shell starts, Bash assigns to it the full pathname of the current user’s login shell.



### SHELLOPTS
A colon-separated list of enabled shell options. Each word in the list is a valid argument 
for `set -o` builtin. The options appearing in SHELLOPTS are those reported as enabled
by `set -o`. If this variable is in the environment when Bash starts up, each shell option 
in the list will be enabled before reading any startup files. This variable is *readonly*.



### SHLVL
Incremented by one each time a new instance of Bash is started. This is intended to be a count of how deeply your Bash shells are nested.



### TIMEFORMAT
The value of this parameter is used as a format string specifying how the timing 
information for pipelines prefixed with the time reserved word should be displayed. 
The `%` character introduces an escape sequence that is expanded to a time value or other 
information. The escape sequences and their meanings are as follows; the braces denote 
optional portions.
```
%% = A literal ‘%’.
%[p][l]R = The elapsed time in seconds.
%[p][l]U = The number of CPU seconds spent in user mode.
%[p][l]S = The number of CPU seconds spent in system mode.
%P = The CPU percentage, computed as (%U + %S) / %R. 
```
The optional `p` is a digit specifying the precision, the number of fractional digits 
after a decimal point. A value of 0 causes no decimal point or fraction to be output. 
At most three places after the decimal point may be specified; values of `p` greater 
than 3 are changed to 3. If `p` is not specified, the value 3 is used. The optional `l` specifies a longer format, including minutes, of the form `MMmSS.FFs`. The value of `p` determines whether or not the fraction is included.If this variable is not set, Bash acts as if it had the value `$'\nreal\t%3lR\nuser\t%3lU\nsys\t%3lS'`. If the value is null, no timing information is displayed. A trailing newline is added when the format string is displayed.



### TMOUT
If set to a value greater than zero, TMOUT is treated as the default timeout for the `read` builtin. The `select` command terminates if input does not arrive after TMOUT seconds when input is coming from a terminal. In an interactive shell, the value is interpreted as the number of seconds to wait for a line of input after issuing the primary prompt. Bash terminates after waiting for that number of seconds if a complete line of input 
does not arrive.



### TMPDIR
If set, Bash uses its value as the name of a directory in which Bash creates temporary files for the shell’s use.



### UID
The numeric real user id of the current user. This variable is *readonly*.

---





## Other, commonly used variables

### TZ
Sets the time zone. The time zone is used to display dates, for example, in the ls -l command. If TZ is not set in the user's environment, the system setting is used. Otherwise, Greenwich Mean Time is used.

Commands that print times (and dates) use this variable to determine the time zone. If the TZ variable is left undefined, the operating system's current time zone setting is used. See timezone for details. On Windows, the MKS Toolkit makes use of the built-in timezone support, and you should not set the TZ environment variable.

### TZDIR
TZ and TZDIR give timezone information used by tzset(3) and through that by functions like ctime(3), localtime(3), mktime(3), strftime(3). See also tzselect(8).


### PRINTER
PRINTER or LPDEST may specify the desired printer to use. See lpr(1).

### LPDEST
PRINTER or LPDEST may specify the desired printer to use. See lpr(1).


### TERM
Defines the terminal. This variable should be reset in either the /etc/profile or /etc/.login file. When the user invokes an editor, the system looks for a file with the same name that is defined in this environment variable. The system searches the directory referenced by TERMINFO to determine the terminal characteristics.


### TERMINFO
Names a directory where an alternate terminfo database is stored. Use the TERMINFO variable in either the /etc/profile or /etc/.login file. For more information, see the terminfo (4) man page.
When the TERMINFO environment variable is set, the system first checks the TERMINFO path defined by the user. If the system does not find a definition for a terminal in the TERMINFO directory defined by the user, it searches the default directory, /usr/share/lib/terminfo, for a definition. If the system does not find a definition in either location, the terminal is identified as "dumb".


### TERMCAP
Database entry of the terminal escape codes to perform various terminal functions.

### LOGNAME
Defines the name of the user that is currently logged in. The default value of LOGNAME is automatically set by the login program to the user name that is specified in the passwd file. You should only need to refer to, not reset, this variable.

### MANPATH
Colon separated list of directories to search for manual pages.

### EDITOR
Set name of default (line) text editor.

### VISUAL
Set name of default (full-screen) text editor.

### BROWSER
Set name of default browser.

### PAGER
Set name of default pager. Default: `pager`

### DISPLAY
Set X display name. `export DISPLAY=:0.1`

### LS_COLORS
ls command's spec for colors

### DOMAIN
domain name

### HOSTALIASES
Gives the name of a file containing aliases to be used with gethostbyname(3).

### XENVIRONMENT
location of your personal settings for X behavior

### XFILESEARCHPATH
paths to search for graphical libraries


---


## XDG Base Directory Specification

https://standards.freedesktop.org/basedir-spec/basedir-spec-latest.html

### XDG_DATA_HOME
defines the base directory relative to which user specific data files should be stored. If $XDG_DATA_HOME is either not set or empty, a default equal to $HOME/.local/share should be used.

### XDG_CONFIG_HOME
defines the base directory relative to which user specific configuration files should be stored. If $XDG_CONFIG_HOME is either not set or empty, a default equal to $HOME/.config should be used.

### XDG_DATA_DIRS
defines the preference-ordered set of base directories to search for data files in addition to the $XDG_DATA_HOME base directory. The directories in $XDG_DATA_DIRS should be seperated with a colon ':'.

If $XDG_DATA_DIRS is either not set or empty, a value equal to /usr/local/share/:/usr/share/ should be used.

### XDG_CONFIG_DIRS
defines the preference-ordered set of base directories to search for configuration files in addition to the $XDG_CONFIG_HOME base directory. The directories in $XDG_CONFIG_DIRS should be seperated with a colon ':'.

If $XDG_CONFIG_DIRS is either not set or empty, a value equal to /etc/xdg should be used.

The order of base directories denotes their importance; the first directory listed is the most important. When the same information is defined in multiple places the information defined relative to the more important base directory takes precedent. The base directory defined by $XDG_DATA_HOME is considered more important than any of the base directories defined by $XDG_DATA_DIRS. The base directory defined by $XDG_CONFIG_HOME is considered more important than any of the base directories defined by $XDG_CONFIG_DIRS.


### XDG_CACHE_HOME
defines the base directory relative to which user specific non-essential data files should be stored. If $XDG_CACHE_HOME is either not set or empty, a default equal to $HOME/.cache should be used.

### XDG_RUNTIME_DIR
defines the base directory relative to which user-specific non-essential runtime files and other file objects (such as sockets, named pipes, ...) should be stored. The directory MUST be owned by the user, and he MUST be the only one having read and write access to it. Its Unix access mode MUST be 0700.

The lifetime of the directory MUST be bound to the user being logged in. It MUST be created when the user first logs in and if the user fully logs out the directory MUST be removed. If the user logs in more than once he should get pointed to the same directory, and it is mandatory that the directory continues to exist from his first login to his last logout on the system, and not removed in between. Files in the directory MUST not survive reboot or a full logout/login cycle.

The directory MUST be on a local file system and not shared with any other system. The directory MUST by fully-featured by the standards of the operating system. More specifically, on Unix-like operating systems AF_UNIX sockets, symbolic links, hard links, proper permissions, file locking, sparse files, memory mapping, file change notifications, a reliable hard link count must be supported, and no restrictions on the file name character set should be imposed. Files in this directory MAY be subjected to periodic clean-up. To ensure that your files are not removed, they should have their access time timestamp modified at least once every 6 hours of monotonic time or the 'sticky' bit should be set on the file.

If $XDG_RUNTIME_DIR is not set applications should fall back to a replacement directory with similar capabilities and print a warning message. Applications should use this directory for communication and synchronization purposes and should not place larger files in it, since it might reside in runtime memory and cannot necessarily be swapped out to disk.



## Locale

locale command without parameters outputs information about the current locale environment.
A list of available locales can be found on UNIX platform by running the locale -a command.

```
LANG=en_US.ISO8859-1 
LC_CTYPE="en_US.ISO8859-1" 
LC_NUMERIC="en_US.ISO8859-1" 
LC_TIME="en_US.ISO8859-1" 
LC_COLLATE="en_US.ISO8859-1" 
LC_MONETARY="en_US.ISO8859-1" 
LC_MESSAGES="en_US.ISO8859-1" 
LC_PAPER="en_US.ISO8859-1" 
LC_NAME="en_US.ISO8859-1" 
LC_ADDRESS="en_US.ISO8859-1" 
LC_TELEPHONE="en_US.ISO8859-1" 
LC_MEASUREMENT="en_US.ISO8859-1" 
LC_IDENTIFICATION="en_US.ISO8859-1" 
LC_ALL=
```

On UNIX-based platforms, The LC_ALL (or LANG) environment variable defines the global settings for the language used by the application.
With the LANG environment variable (or LC_ALL, on UNIX), you define the language, the territory (aka country) and the codeset (aka character set or code page) to be used. The format of the value is normalized as follows, but may be specific on some operating systems:
`language_territory.codeset`  
For example: `export LC_ALL=en_US.iso88591`  


---

## Application-specific environment variables

Programs like `make` and `autoconf` allow overriding of default utility names from the environment with similarly named variables in all caps. Thus one uses `CC` to select the desired C compiler (and similarly `MAKE, AR, AS, FC, LD, LEX, RM, YACC`, etc.). 

However, in some traditional uses such an environment variable gives **options** for the program instead of a pathname, like with `MORE`, `LESS`, and `GZIP`.

