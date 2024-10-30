# About environment variables

The only difference between shell variables and environment variables is that the latter have the `x` (export) attribute set. This attribute may be set at variable declaration time, `declare -x VAR`, or later with `export VAR`.

Besides shell variables, shell functions can also be exported. Functions can be assigned the `x` attribute with `export` builtin, `export fname`.

To remove the `x` attribute from variables use `declare +x VAR` or `export -n VAR`. 


## Creating environment variables

A regular shell variable may be created in several ways, one of which is the degenerate form of command called the *assignment statement*.

 which has the form, `NAME=VALUE`, and appears alone on a command line. Curiously, assignment statement is not a command, it 



New vars
- use `declare` builtin: `declare -x NAME=VALUE`
- use `export` builtin: `export NAME=VALUE`

If you want to define a new environment variable


- use assignment statement `NAME=VALUE`, then `export NAME`

if var `NAME` already exists, perhaps declared
Existing vars:
- use `declare` builtin to add the 'x' attribute: `declare -x NAME`


```bash
# seemingly infinite expansion:
A=1=2
echo $A
1=2
echo $A=
1=2=
echo $A=1
1=2=1
echo $A=1=
1=2=1=
…
```


## Who sets env vars
Some variables were obtained through inheritence from the parent process. Some were set by the system, some by the terminal, and some by bash. Most were set by the user.

## Setting environment variables in different shells

The way you set environment variables is dependent on your shell. 
Assuming you want to set the `DUCK` variable to `1`:

* Bash
Add this to your configuration (usually ~/.bashrc):

    export DUCK=1

* cmd.exe (with Clink)
Add this to your configuration (find it by running clink info in cmd.exe): 

    set DUCK=1

* Elvish
Add this to your configuration (usually ~/.elvish/rc.elv): 

    set E:DUCK = '1'

* Fish
Add this to your configuration (usually ~/.config/fish/config.fish):

    set -x DUCK '1'

* Nushell
Add this to your configuration (find it by running config path in Nushell): 

    [env]
    DUCK = "1"

* PowerShell
Add this to your configuration (find it by running echo $profile in PowerShell):

    $env:DUCK = '1'

* Xonsh
Add this to your configuration (usually ~/.xonshrc): 

    $DUCK = '1'

* Any POSIX shell
Add this to your configuration: 

    export DUCK='1'
