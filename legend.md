# Environment Variables :: Legend

- logically, envars are key-value pairs, `name=value`
- envars are exported shell variables, i.e. shell vars with the `x` attribute
- shell functions may also be considered a kind of envars
- arrays are never envars because they cannot be exported
- there is a set of standard, common, envars that many agents consult
- envars are a way to affect the behavior of apps that choose to allow it
- CLIs may create own set of envars, but consult a bigger set

- creating
- consulting

## Workings

In the shell, environment variables are exported shell variables, i.e. variables with the `x` attribute.

## Export builtin

- `export` builtin is used to export shell variables, `export NAME …`
- remove the export attribute: `export -n NAME`


>export [-fn] [name[=value] ...] or export -p

Set export attribute for shell variables.

Marks each NAME for **automatic export to the environment of subsequently executed commands**. If VALUE is supplied, assign VALUE before exporting.

Options:
- `-f` Refer to shell functions
- `-n` Remove the export property from each NAME
- `-p` Display a list of all exported variables and functions

An argument of `--` disables further option processing.



Exit Status:
- 0 success
- 1 invalid NAME¹
- 2 invalid option

¹ WARNING: Well-formed but non-existent NAMES will be exported anyway with no value.


it is not easy to come up with a name (of NAME) that 




Environment variables are qualified, divideds, classified, sorted according to attributes, properties, aspects.

## Factors of division
- purpose
- scope
- origin
- special status
- readonly or fragile (loose their special property)
- by types of values
- user-definable
- user-writeable
- set by the shell
- shell-defined
- introduced in sh
- introduced in bash
- POSIX special envar


## Logical value types

There is only a single type of value - raw untyped string - but logically, it may be interpreted as the following types:

- String
  - number
  - path (filename, dirname)
  - sequence of characters (IFS, $-)
  - Delimited values ("compound" values, lists)
    - semi-colon-separated values (PROMPT_COMMAND)
    - colon-separated values
      - colon-separated dirs (PATH)
    - key-value pairs ()
    - comma-separated values

- sadly, there is no compound type `Set`, so PATH duplicates must be managed manually. zsh maintains two versions of some envars including PATH: one is the traditional `PATH` envar that contains colon-delimited values and the other is the `path` indexed-array; what's great is that zsh maintains their synchronization.
- some env vars are *magical* (RANDOM, ): if the user deletes them or sets them to null they loose their magic properties




## Sample

PROMPT_COMMAND=history -a; history -n;

HOSTTYPE=x86_64
LANG=C.UTF-8
LC_CTYPE=C.UTF-8
LOGNAME=ivan
COLORTERM=truecolor
EDITOR=vim
FUNCNEST=100
HISTFILESIZE=10000
HISTSIZE=10000
MAILCHECK=0
MANPAGER=most
NAME=drivan
SHLVL=0
TERM=xterm-256color
USER=ivan
VISUAL=vim
WAYLAND_DISPLAY=wayland-0
WSL2_GUI_APPS_ENABLED=1
WSL_DISTRO_NAME=ubuntu2205
WSL_GUEST_IP=172.29.72.89
WSL_HOST_IP=172.29.64.1

BROWSER
PAGER
VISUAL
HOME=/home/ivan
PWD=/home/ivan/proj/bash/shartefacts/scripts/elgyn
OLDPWD=/home/ivan
SHELL=/bin/bash
XDG_RUNTIME_DIR=/run/user/1000/
WSL_INTEROP=/run/WSL/4538_interop
_=/usr/bin/printenv


DISPLAY=:0
DISPLAY=192.168.0.1:0
DBUS_SESSION_BUS_ADDRESS=unix:path=/run/user/1000/bus
PULSE_SERVER=unix:/mnt/wslg/PulseServer

PATH=.:/bin::/usr/sbin:/usr/bin:/sbin:/usr/games:
XDG_DATA_DIRS=/usr/local/share:/usr/share:/var/lib/snapd/desktop
EXECIGNORE=/c/**:/t/**:/v/**:/mnt/**
FIGNORE=.exe:.dll:.cpl:mmc
GLOBIGNORE=*.exe:*.dll:*.cpl:*mmc
HISTCONTROL=ignorespace:ignoredups
LS_COLORS=no=0:fi=0:rs=0:di=0:ln=3:pi=3:so=3:do=3:bd=3:cd=3:or=3:mi=3:mh=3:ow=3:su=0:sg=0:ca=0:tw=0:st=0:ex=0:
