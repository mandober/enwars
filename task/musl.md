# Environment Variables :: musl 1.1.24


## PATH
Used by execvp, execlp, and posix_spawnp as specified in POSIX. If unset, a default search path of `"/usr/local/bin:/bin:/usr/bin"` is used.

## TZ
Specifies the local timezone to be used for functions which deal with local time. The value of `TZ` can be either a POSIX timezone specification in the form `stdoffset[dst[offset][,start[/time],end[/time]]]` or the name of a zoneinfo-binary-format timezone file (the form used by glibc and most other systems). The latter is interpreted as an absolute pathname if it begins with a slash, a relative pathname if it begins with a dot, and otherwise is searched in `/usr/share/zoneinfo`, `/share/zoneinfo`, and `/etc/zoneinfo`. When searching these paths, strings including any dots are rejected. If the program was invoked setuid, setgid, or with other elevated capabilities, the absolute and relative pathname options are not available.

## DATEMSK
Used by the `getdate` function as a pathname for the file containing date formats to scan, per POSIX.

## MSGVERB
Used by the `fmtmsg` function to control message verbosity.

## PWD
Used by the nonstandard `get_current_dir_name` function; if it matches the actual current directory, it is returned instead of using `getcwd` to obtain the canonical pathname.

## LOGNAME
The `getlogin` function simply returns the value of the `LOGNAME` variable.

## LD_PRELOAD
Colon-separated list of shared libraries that will be preloaded by the dynamic linker before processing the application's dependency list. Components can be absolute or relative pathnames or filenames in the default library search path. This variable is completely ignored in programs invoked setuid, setgid, or with other elevated capabilities.

## LD_LIBRARY_PATH
Colon-separated list of pathnames that will be searched for shared libraries requested without an explicit pathname. This path is searched prior to the default path (which is specified in `$(syslibdir)/../etc.ld-musl-$(ARCH).path` with built-in default fallback if this file is missing). This variable is completely ignored in programs invoked setuid, setgid, or with other elevated capabilities.

## LC_✱

- `LC_ALL`
- `LC_CTYPE`
- `LC_NUMERIC`
- `LC_TIME`
- `LC_COLLATE`
- `LC_MONETARY`
- `LC_MESSAGES`
- `LANG`

Used by `setlocale` and `newlocale` to determine a locale name to use when a zero-length string is passed. The precedence rules follow POSIX: `LC_ALL` overrides category-specific variables, and `LANG` provides a default for any category not set.

## MUSL_LOCPATH
Colon-separated list of paths that will be searched for locale definitions. The requested locale name string will used as a filename and searched in each path component. If unset, locale files are not loaded and only the "C" locale is available. This variable is completely ignored in programs invoked setuid, setgid, or with other elevated capabilities.
