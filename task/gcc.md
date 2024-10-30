## Environment Variables :: GCC

## Overview

- GCC specific env vars
  - GCC_COMPARE_DEBUG
  - GCC_EXEC_PREFIX
  - GCC_EXTRA_DIAGNOSTIC_OUTPUT
  - COMPILER_PATH
  - LIBRARY_PATH
- Env vars that affect preprocessor
  - CPATH
  - C_INCLUDE_PATH
  - CPLUS_INCLUDE_PATH
  - OBJC_INCLUDE_PATH
  - DEPENDENCIES_OUTPUT
  - SUNPRO_DEPENDENCIES
  - SOURCE_DATE_EPOCH
- Other environment variables
  - LC_MESSAGES
  - LC_CTYPE
  - LC_ALL
  - LANG
  - TMPDIR


https://gcc.gnu.org/onlinedocs/gcc/Environment-Variables.html

These environment variables affect how GCC operates. Some of them work by specifying directories or prefixes to use when searching for various kinds of files. Some are used to specify other aspects of the compilation environment. You can also specify places to search using options like `-B`, `-I` and `-L`. These take precedence over places specified using env vars, which in turn take precedence over those specified by the configuration of GCC.

## Contents

- [GCC specific env vars](#gcc-specific-env-vars)
  - [GCC_COMPARE_DEBUG](#gcc_compare_debug)
  - [GCC_EXEC_PREFIX](#gcc_exec_prefix)
  - [GCC_EXTRA_DIAGNOSTIC_OUTPUT](#gcc_extra_diagnostic_output)
  - [COMPILER_PATH](#compiler_path)
  - [LIBRARY_PATH](#library_path)
- [Env vars that affect preprocessor](#env-vars-that-affect-preprocessor)
  - [CPATH](#cpath)
  - [C_INCLUDE_PATH](#c_include_path)
  - [CPLUS_INCLUDE_PATH](#cplus_include_path)
  - [OBJC_INCLUDE_PATH](#objc_include_path)
  - [DEPENDENCIES_OUTPUT](#dependencies_output)
  - [SUNPRO_DEPENDENCIES](#sunpro_dependencies)
  - [SOURCE_DATE_EPOCH](#source_date_epoch)
- [Other environment variables](#other-environment-variables)
  - [LC_MESSAGES](#lc_messages)
  - [LC_CTYPE](#lc_ctype)
  - [LC_ALL](#lc_all)
  - [LANG](#lang)
  - [TMPDIR](#tmpdir)


## GCC specific env vars

### GCC_COMPARE_DEBUG
Setting GCC_COMPARE_DEBUG is nearly equivalent to passing `-fcompare-debug` to the compiler driver.

### GCC_EXEC_PREFIX
If set, it specifies a prefix to use in the names of the subprograms executed by the compiler. No slash is added when this prefix is combined with the name of a subprogram, but you can specify a prefix that ends with a slash. If GCC_EXEC_PREFIX is not set, GCC attempts to figure out an appropriate prefix to use based on the pathname it is invoked with. If GCC cannot find the subprogram using the specified prefix, it tries looking in the usual places for the subprogram. The default value of GCC_EXEC_PREFIX is `prefix/lib/gcc/`, where 'prefix' is the prefix to the installed compiler. In many cases prefix is the value of 'prefix' when you ran the configure script. Other prefixes specified with `-B` take precedence over this prefix. This prefix is also used for finding files such as `crt0.o` that are used for linking.

Additionally, the prefix is used in an unusual way in finding the directories to search for *header files*. For each of the standard directories whose name normally begins with `/usr/local/lib/gcc` (more precisely, with the value of `GCC_INCLUDE_DIR`), GCC tries replacing that beginning with the specified prefix to produce an alternate directory name. Thus, with `-Bfoo/`, GCC searches `foo/bar` just before it searches the standard directory `/usr/local/lib/bar`. If a standard directory begins with the configured prefix then the value of prefix is replaced by GCC_EXEC_PREFIX when looking for *header files*.

### GCC_EXTRA_DIAGNOSTIC_OUTPUT
If set to one of the following values, additional text will be emitted to stderr when fix-it hints are emitted. `-fdiagnostics-parseable-fixits` and `-fno-diagnostics-parseable-fixits` take precedence over this env var.
- `fixits-v1` Emit parseable fix-it hints, equivalent to `-fdiagnostics-parseable-fixits`. In particular, columns are expressed as a count of bytes, starting at byte 1 for the initial column.
- `fixits-v2` As fixits-v1, but columns are expressed as display columns, as per `-fdiagnostics-column-unit=display`.

### COMPILER_PATH
The value of COMPILER_PATH is a colon-separated list of directories, much like PATH. GCC tries the directories thus specified when searching for subprograms, if it cannot find the subprograms using GCC_EXEC_PREFIX.

### LIBRARY_PATH
The value of LIBRARY_PATH is a colon-separated list of directories, much like PATH. When configured as a native compiler, GCC tries the directories thus specified when searching for special linker files, if it cannot find them using GCC_EXEC_PREFIX. Linking using GCC also uses these directories when searching for ordinary libraries for the `-l` option (but directories specified with `-L` come first).

## Env vars that affect preprocessor

### CPATH
Its value is a list of directories separated by a special character, much like PATH, in which to look for *header files*. This env var is used regardless of which language is being preprocessed.

`CPATH` specifies a list of directories to be searched as if specified with `-I`, but after any paths given with `-I` options on the command line. 

The list of directories is searched as if specified with `-isystem`, but after any paths given with `-isystem` options on the command line.

An empty element instructs the compiler to search the cwd. Empty elements can appear at the beginning or end of a path. For instance, if the value of CPATH is `:/special/include`, that has the same effect as `-I. -I/special/include`.


### C_INCLUDE_PATH
Its value is a list of directories separated by a special character, much like PATH, in which to look for *header files*. This env var is used only when preprocessing C.

An empty element instructs the compiler to search the cwd. Empty elements can appear at the beginning or end of a path.

The list of directories is searched as if specified with `-isystem`, but after any paths given with `-isystem` options on the command line.


### CPLUS_INCLUDE_PATH
Its value is a list of directories separated by a special character, much like PATH, in which to look for *header files*.

An empty element instructs the compiler to search the cwd. Empty elements can appear at the beginning or end of a path.

This env var is used only when C++ is being preprocessed.

The list of directories is searched as if specified with `-isystem`, but after any paths given with `-isystem` options on the command line.

### OBJC_INCLUDE_PATH

Its value is a list of directories separated by a special character, much like PATH, in which to look for *header files*.

An empty element instructs the compiler to search the cwd. Empty elements can appear at the beginning or end of a path.

This env var is used only when ObjC is being preprocessed.

The list of directories is searched as if specified with `-isystem`, but after any paths given with `-isystem` options on the command line.



### DEPENDENCIES_OUTPUT
If set, its value specifies how to output dependencies for Make, based on the non-system *header files* processed by the compiler. System *header files* are ignored in the dependency output.

The value of DEPENDENCIES_OUTPUT can be just a file name, in which case the Make rules are written to that file, guessing the target name from the source file name. Or the value can have the form 'file target', in which case the rules are written to file file using 'target' as the target name.

In other words, this env var is equivalent to combining the options `-MM` and `-MF` (see Options Controlling the Preprocessor), with an optional `-MT` switch.

### SUNPRO_DEPENDENCIES
This variable is the same as DEPENDENCIES_OUTPUT except that system *header files* are not ignored, so it implies `-M` rather than `-MM`. However, the dependence on the main input file is omitted.

### SOURCE_DATE_EPOCH
If set, it specifies a UNIX timestamp to be used in replacement of the current date and time in the `__DATE__` and `__TIME__` macros, so that the embedded timestamps become reproducible. The value of SOURCE_DATE_EPOCH must be a UNIX timestamp, defined as the number of seconds (excluding leap seconds) since 01 Jan 1970 00:00:00 represented in ASCII; identical to the output of `date +%s` on GNU/Linux and other systems that support the `%s` extension in `date`. The value should be a known timestamp such as the last modification time of the source or package and it should be set by the build process.

## Other env vars

### LC_MESSAGES
LC_MESSAGES specifies the language to use in diagnostic messages.

### LC_CTYPE
LC_CTYPE specifies character classification. GCC uses it to determine the character boundaries in a string; this is needed for some multibyte encodings that contain quote and escape characters that are otherwise interpreted as a string end or escape.

### LC_ALL
If LC_ALL is set, it overrides the value of LC_CTYPE and LC_MESSAGES; otherwise, LC_CTYPE and LC_MESSAGES default to the value of the LANG. If none of these are set, GCC defaults to traditional C English behavior.

The LANG, LC_CTYPE, LC_MESSAGES and LC_ALL environment variables control the way that GCC uses localization information which allows GCC to work with different national conventions. GCC inspects the locale categories LC_CTYPE and LC_MESSAGES if it has been configured to do so. These locale categories can be set to any value supported by your installation. A typical value is 'en_GB.UTF-8' for English in the United Kingdom encoded in UTF-8.

### LANG
LANG is used to pass locale information to the compiler. One aspect of what this information affects is the character set when character literals, string literals and comments are parsed in C and C++. When the compiler is configured to allow multibyte characters, the following values for LANG are recognized:
- `C-JIS`   Recognize JIS characters.
- `C-SJIS`  Recognize SJIS characters.
- `C-EUCJP` Recognize EUCJP characters.

If LANG is not defined, or if it has some other value, then the compiler uses `mblen` and `mbtowc` as defined by the default locale to recognize and translate multibyte characters. LANG is consulted as the lowest precedence overrider, consulted only if LC_ALL is unset.

### TMPDIR
If TMPDIR is set, it specifies the directory to use for temporary files. GCC uses temporary files to hold the output of one stage of compilation which is to be used as input to the next stage: for example, the output of the preprocessor, which is the input to the compiler proper.
