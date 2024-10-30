# Environment Variables :: Bash

Classes of env vars used in bash:
- inhereted from Bourne shell
- Env vars set by bash
- read by bash
- considered by bash

## Env vars set by bash

## BASH
- desc: The full pathname used to execute the current instance of bash.
- type: path
- e.g. `BASH=/bin/bash`


## BASHOPTS
List of enabled shell options. Each word in the list is a valid argument for `shopt -s|-u`. If this variable is in the environment when Bash starts up, each shell option in the list will be enabled before reading any startup files.  
> Shell: bash  
> Type: colon-separated values  
> Attributes: readonly  
> Example: `BASHOPTS=dotglob:extglob:extquote:globstar:lastpipe`  

## BASHPID
Expands to the process ID of the current Bash process. This differs from `$$` under certain circumstances, such as subshells that do not require Bash to be re-initialized.  
> Shell: bash  
> Type: integer  
> Attributes: readonly  

## BASH_ALIASES
An associative array whose members correspond to the internal list of aliases as maintained by the alias builtin. Elements added to this array will appear in the alias list; however, unsetting elements does not cause aliases to be removed.  
> Shell: bash  
> Type: associative array  
> Attributes: special  
> Example: `BASH_ALIASES=([pp]="echo ${PATH//:/$'\f\r'}")`  

## BASH_ARGC
An array whose values are the number of parameters in each frame of the current bash execution call stack. The number of parameters to the current subroutine (shell function or script executed with `source`) is at the top of the stack. When a subroutine is executed, the number of parameters passed is pushed onto BASH_ARGC. The shell sets BASH_ARGC only when in extended debugging mode.  
> Shell: bash  
> Type: indexed array  
> Context: debugging  

## BASH_ARGV
An array containing all of the parameters in the current bash execution call stack. The final parameter of the last subroutine call is at the top of the stack; the first parameter of the initial call is at the bottom. When a subroutine is executed, the parameters supplied are pushed onto BASH_ARGV. The shell sets BASH_ARGV only when in extended debugging mode.  
> Shell: bash  
> Type: indexed array  
> Context: debugging  

## BASH_CMDS
An associative array variable whose members correspond to the internal hash table of commands as maintained by the `hash` builtin. Elements added to this array appear in the hash table; however, unsetting array elements currently does not cause command names to be removed from the hash table.  
> Shell: bash  
> Type: associative array  
> Attributes: special  

## BASH_COMMAND
The command currently being executed or about to be executed, unless the shell is executing a command as the result of a trap, in which case it is the command executing at the time of the trap.  
> Shell: bash  
> Context: debugging  

## BASH_COMPAT
The value is used to set the shell’s compatibility level. The value may be a decimal number (4.2) or an integer (42) corresponding to the desired compatibility level. If unset or set to null string, the compatibility level is set to current version. If set to invalid string, the shell prints an error and sets the compatibility level to current version. Accepted values: 31, 32, 40, 41, 42, 43, 44
> Shell: bash  
> Context: compatibility  

## BASH_ENV
If set, its value (subject to parameter expansion, command substitution, and arithmetic expansion) is interpreted as a filename to a file that will be sourced in the same environment as the script about to be executed. BASH_ENV has to be exported and resultant filename has to be absolute.  
> Shell: bash  
> Context: hook  
> Example: `export BASH_ENV=$HOME/pre-script-hook`  

## BASH_EXECUTION_STRING
The command argument to the -c invocation option.
> Shell: bash  

## BASH_LINENO
An array variable whose members are the line numbers in source files where each corresponding member of FUNCNAME was invoked. ${BASH_LINENO[$i]} is the line number in the source file (${BASH_SOURCE[$i+1]}) where ${FUNCNAME[$i]} was called (or ${BASH_LINENO[$i-1]} if referenced within another shell function). Use LINENO to obtain the current line number.
> Shell: bash  
> Context: debugging  

## BASH_LOADABLES_PATH
A colon-separated list of directories in which the shell looks for dynamically loadable builtins specified by the enable command.
> Shell: bash  

## BASH_REMATCH
An array variable whose members are assigned by the ‘=~’ binary operator to the [[ conditional 
command. The element with index 0 is the portion of the string matching the entire 
regular expression. The element with index n is the portion of the string matching the 
nth parenthesized subexpression. This variable is READ-ONLY.
> Shell: bash  

## BASH_SOURCE
An array variable whose members are the source filenames where the corresponding shell function names in the FUNCNAME array variable are defined. The shell function ${FUNCNAME[$i]} is defined in the file ${BASH\_SOURCE[$i]} and called from ${BASH_SOURCE[$i+1]}
> Shell: bash  

## BASH_SUBSHELL
Incremented by one within each subshell or subshell environment when the shell begins executing in that environment. The initial value is 0.
> Shell: bash  

## BASH_VERSINFO
A readonly array variable (see Arrays) whose members hold version information for this instance of Bash. The values assigned to the array members are as follows:
> Shell: bash  

## BASH_VERSINFO
BASH_VERSINFO[0] - The major version number (the release).  
BASH_VERSINFO[1] - The minor version number (the version).  
BASH_VERSINFO[2] - The patch level.  
BASH_VERSINFO[3] - The build version.  
BASH_VERSINFO[4] - The release status (e.g., beta1).
BASH_VERSINFO[5] - The value of MACHTYPE.  
> Shell: bash  

## BASH_VERSION
The version number of the current instance of Bash.
> Shell: bash  

## BASH_XTRACEFD
If set to an integer corresponding to a valid file descriptor, Bash will write the trace output generated when ‘set -x’ is enabled to that file descriptor. This allows tracing output to be separated from diagnostic and error messages. The file descriptor is closed when BASH\_XTRACEFD is unset or assigned a new value. Unsetting BASH\_XTRACEFD or assigning it the empty string causes the trace output to be sent to the standard error. Note that setting BASH_XTRACEFD to 2 (the standard error file descriptor) and then unsetting it will result in the standard error being closed.
> Shell: bash  
