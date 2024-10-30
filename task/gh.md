# gh environment variables

https://cli.github.com/manual/gh_help_environment

`gh` - GitHub's official command line tool.

## Index of envars - all consulted envars


```
{GH,GITHUB}_TOKEN
{GH,GITHUB}_ENTERPRISE_TOKEN

GH_TOKEN
GITHUB_TOKEN
GH_ENTERPRISE_TOKEN
GITHUB_ENTERPRISE_TOKEN

GH_HOST
GH_REPO

GH_EDITOR
GIT_EDITOR
VISUAL
EDITOR

GH_BROWSER
BROWSER

GH_DEBUG
DEBUG (deprecated)

GH_PAGER
PAGER

GLAMOUR_STYLE
NO_COLOR
CLICOLOR
CLICOLOR_FORCE

GH_FORCE_TTY
GH_NO_UPDATE_NOTIFIER
GH_CONFIG_DIR
GH_PROMPT_DISABLED
GH_PATH
```

## Index of envars - only own envars

GH_{TOKEN,ENTERPRISE_TOKEN,HOST,REPO,EDITOR,BROWSER,DEBUG,PAGER,FORCE_TTY,NO_UPDATE_NOTIFIER,CONFIG_DIR,PROMPT_DISABLED,PATH}

GH_TOKEN
GH_ENTERPRISE_TOKEN
GH_HOST
GH_REPO
GH_EDITOR
GH_BROWSER
GH_DEBUG
GH_PAGER
GH_FORCE_TTY
GH_NO_UPDATE_NOTIFIER
GH_CONFIG_DIR
GH_PROMPT_DISABLED
GH_PATH



## Description of envars

GH_TOKEN GITHUB_TOKEN (in order of precedence)    
Authentication token for github.com API requests. Setting this avoids being prompted to authenticate and takes precedence over previously stored credentials.

GH_ENTERPRISE_TOKEN GITHUB_ENTERPRISE_TOKEN (in order of precedence)    
An authentication token for API requests to GitHub Enterprise. 
When setting this, also set GH_HOST.

GH_HOST   
Specify the GitHub hostname for commands that would otherwise assume github.com host when not in a context of an existing repository. When setting this, also set GH_ENTERPRISE_TOKEN.

GH_REPO
Specify the GitHub repository in the `[HOST/]OWNER/REPO` format for commands that otherwise operate on a local repository.

GH_EDITOR
GIT_EDITOR
VISUAL
EDITOR
(in order of precedence)
The editor tool to use for authoring text.

GH_BROWSER
BROWSER
(in order of precedence)
The web browser to use for opening links.

GH_DEBUG
Set to a truthy value to enable verbose output on standard error.
Set to `api` to additionally log details of HTTP traffic.

DEBUG
(deprecated)
Set to 1, true, or yes to enable verbose output on standard error.

GH_PAGER
PAGER
(in order of precedence)
A terminal paging program to send standard output to (e.g. less)

GLAMOUR_STYLE
The style to use for rendering Markdown. 
See https://github.com/charmbracelet/glamour#styles

NO_COLOR
Set to any value to avoid printing *ANSI escape sequences* for color output.

CLICOLOR
Set to 0 to disable printing ANSI colors in output.

CLICOLOR_FORCE
Set to a value other than 0 to keep ANSI colors in output even when the output is piped.

GH_FORCE_TTY
Set to any value to force terminal-style output even when the output is redirected. When the value is a number, it is interpreted as the number of columns available in the viewport. When the value is a percentage, it will be applied against the number of columns available in the current viewport.

GH_NO_UPDATE_NOTIFIER
Set to any value to disable update notifications. By default, gh checks for new releases once every 24 hours and displays an upgrade notice on standard error if a newer version was found.

GH_CONFIG_DIR
The directory where gh will store configuration files. If not specified, the default value will be one of the following paths (in order of precedence):
- $XDG_CONFIG_HOME/gh (if $XDG_CONFIG_HOME is set)
- $AppData/GitHub CLI (on Windows if $AppData is set), or
- $HOME/.config/gh

GH_PROMPT_DISABLED
Set to any value to disable interactive prompting in the terminal.

GH_PATH
Set the path to the gh executable, useful when gh can not properly determine its own path, like in the Cygwin terminal.
