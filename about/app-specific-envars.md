# Application-specific environment variables

Some common *use patterns* of envars in different utilities.
- overriding of default utility names
- specifying command-line options
- specifying configuration options

## Overriding of default utility names

Programs like `make` and `autoconf` allow overriding of default utility names from the environment with similarly named variables in all caps. Thus one uses `CC` to select the desired C compiler; and similarly `MAKE, AR, AS, FC, LD, LEX, RM, YACC`, etc.

## Specifying default command-line options

Another traditional use pattern is to specify default arguments for a program. In this use, the name of the program matches the name of environment variable, case-insensitively; i.e. env var name is usually in all caps.

Such an environment variable gives options for the program instead of a pathname, like with `MORE`, `LESS`, and `GZIP`.

Options set by env var can be overriden on the command line (using e.g. options prefixed with `+` to turn off set options).

## Specifying configuration options

Some programs allow specifying configuration option in envars. The name of an envar corresponds to a config option (adjusting the letter case and separator). git is one program that does this; for example, the command-line option `--git-dir=PATH` sets the path to the repository (`.git` directory), and the same can also be controlled by setting the `GIT_DIR=PATH` env var.
