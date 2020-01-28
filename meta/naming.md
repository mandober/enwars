# FS Naming system

Naming scheme is set wrt the subject, which, in majority of cases, means a (regular) file or a directory.

1. Considering a regular file: `/etc/default/include.d/info.txt`

Since the subject is a regular file (-f):
- file name or filename: info.txt
- file stem:      info
- file suffix:    txt (or .txt)
- file parent:    include.d
- file directory: include.d
- file pathname:  /etc/default/include.d/
- file path:      /etc/default/include.d/info.txt

2. Considering a directory: `/etc/default/include.d/`
- directory name:     include.d
- directory stem:     include
- directory suffix:   d or .d
- directory's parent: /default/
- directory's path:   /etc/default/
