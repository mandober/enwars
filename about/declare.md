# declare

declare: declare [-aAfFgiIlnrtux] [-p] [name[=value] ...]

Set variable values and attributes.

Declare variables and give them attributes.  If no NAMEs are given,
display the attributes and values of all variables.

Options:

-f        restrict action or display to function names and definitions

-F        restrict display to function names only 
          (plus line number and source file when debugging)

-g        create global variables when used in a shell function; 
          otherwise ignored

-I        if creating a local variable, inherit the attributes and value
          of a variable with the same name at a previous scope

-p        display the attributes and value of each NAME

Options which set attributes:

-a        to make NAMEs indexed arrays (if supported)
-A        to make NAMEs associative arrays (if supported)
-i        to make NAMEs have the `integer` attribute
-l        to convert the value of each NAME to lower case on assignment
-n        make NAME a reference to the variable named by its value
-r        to make NAMEs readonly
-t        to make NAMEs have the `trace` attribute
-u        to convert the value of each NAME to upper case on assignment
-x        to make NAMEs export

Using `+` instead of `-` turns off the given attribute.

Variables with the integer attribute have arithmetic evaluation (see the `let` command) performed when the variable is assigned a value.

When used in a function, `declare` makes NAMEs local, as with the `local` command. The `-g` option suppresses this behavior.

## Exit status

Returns
- 0 success, unless
- 1 variable assignment error occured
- 2 invalid option supplied
