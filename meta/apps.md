Application-specific environment variables

Programs like `make` and `autoconf` allow overriding of default utility names from the environment with similarly named variables in all caps. Thus one uses `CC` to select the desired C compiler (and similarly `MAKE, AR, AS, FC, LD, LEX, RM, YACC`, etc.). 

However, in some traditional uses such an environment variable gives options for the program instead of a pathname, like with `MORE`, `LESS`, and `GZIP`.
