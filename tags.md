## Environment Variables :: Tags

Shell
- bourne-shell
- bash
- ksh

Properties


Values
- plain value
- compound value
- with special property (if unset looses the special property)
- plain value: path, filename, number, string
- compound value: list of items
- glob, wildcard
- defined shell function
- shell variable

Separator
- one separator
- two separators:
  - top level sep: `:`
  - nested level sep: `;`
  - e.g.
    - unix:path=/run/user/1000/bus
    - LS_COLORS=no=0:fi=0:rs=0:di=2:ln=33:pi=92:so=3:do=3:bd=94 …
- list
  - sequence of characters
  - sequence of dirs
    - comma-separated
    - colon-separated
