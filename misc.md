dev-env-vars

# Environment variables

List of common environment variables related to web development.




*BABEL*

* `BABEL_CACHE_PATH` - Specify different location for Babel's cache.
    [https://babeljs.io/docs/usage/babel-register/]
```sh
$ BABEL_CACHE_PATH=/foo/my-cache.json babel-node script.js
```

* `BABEL_DISABLE_CACHE` - Disable Babel's cache.
    [https://babeljs.io/docs/usage/babel-register/]
```sh
$ BABEL_DISABLE_CACHE=1 babel-node script.js
```


*GIT*
https://git-scm.com/book/tr/v2/Git-Internals-Environment-Variables


*MERCURIAL*

[https://www.selenic.com/mercurial/hg.1.html#environment-variables]
    

Mercurial Environment Variables

HG
    Path to 'hg' executable, automatically passed when running hooks, extensions or external tools. If unset or empty, this is the hg executable's name if it's frozen, or an executable named 'hg' (with %PATHEXT% [defaulting to COM/EXE/BAT/CMD] extensions on Windows) is searched.

HGEDITOR
    This is the name of the editor to run when committing. See EDITOR. (deprecated, use configuration file)
    
HGENCODING
    This overrides the default locale setting detected by Mercurial. This setting is used to convert data including usernames, changeset descriptions, tag names, and branches. This setting can be overridden with the --encoding command-line option.
    
HGENCODINGMODE
    This sets Mercurial's behavior for handling unknown characters while transcoding user input. The default is "strict", which causes Mercurial to abort if it can't map a character. Other settings include "replace", which replaces unknown characters, and "ignore", which drops them. This setting can be overridden with the --encodingmode command-line option.
    
HGENCODINGAMBIGUOUS
    This sets Mercurial's behavior for handling characters with "ambiguous" widths like accented Latin characters with East Asian fonts. By default, Mercurial assumes ambiguous characters are narrow, set this variable to "wide" if such characters cause formatting problems.
    
HGMERGE
    An executable to use for resolving merge conflicts. The program will be executed with three arguments: local file, remote file, ancestor file. (deprecated, use configuration file)
    
HGRCPATH
    A list of files or directories to search for configuration files. Item separator is ":" on Unix, ";" on Windows. If HGRCPATH is not set, platform default search path is used. If empty, only the .hg/hgrc from the current repository is read. For each element in HGRCPATH: if it's a directory, all files ending with .rc are added. Otherwise, the file itself will be added

HGPLAIN
    When set, this disables any configuration settings that might change Mercurial's default output. This includes encoding, defaults, verbose mode, debug mode, quiet mode, tracebacks, and localization. This can be useful when scripting against Mercurial in the face of existing user configuration. Equivalent options set via command line flags or environment variables are not overridden.
    
HGPLAINEXCEPT
    This is a comma-separated list of features to preserve when HGPLAIN is enabled. Currently the following values are supported: alias (Don't remove aliases); i18n (Preserve internationalization); revsetalias (Don't remove revset aliases); templatealias (Don't remove template aliases); progress (Don't hide progress output). Setting HGPLAINEXCEPT to anything (even an empty string) will enable plain mode.
    
HGUSER
    This is the string used as the author of a commit. If not set, available values will be considered in this order: HGUSER (deprecated); configuration files from the HGRCPATH; EMAIL; interactive prompt; LOGNAME (with @hostname appended). (deprecated, use configuration file)

EMAIL
    May be used as the author of a commit; see HGUSER.
    
LOGNAME
    May be used as the author of a commit; see HGUSER.
    
VISUAL
    This is the name of the editor to use when committing. See EDITOR.
    
EDITOR
    Sometimes Mercurial needs to open a text file in an editor for a user to modify, for example when writing commit messages. The editor it uses is determined by looking at the environment variables HGEDITOR, VISUAL and EDITOR, in that order. The first non-empty one is chosen. If all of them are empty, the editor defaults to 'vi'.
    
PYTHONPATH
    This is used by Python to find imported modules and may need to be set appropriately if this Mercurial is not installed system-wide.



*METEOR*
List of environment variables that you can use with your Meteor application.

BIND_IP (production)
Bind the application server to a specific network interface by IP address, 
for example: BIND_IP=192.168.0.2. See also: PORT.
In development, this can be accomplished with meteor run --port a.b.c.d:port.

DISABLE_WEBSOCKETS (development, production)

In the event that your own deployment platform does not support WebSockets, or you 
are confident that you will not benefit from them, setting this variable with 
DISABLE_WEBSOCKETS=1 will explicitly disable WebSockets and forcibly resort to the 
fallback polling-mechanism, instead of trying to detect this automatically.

HTTP_FORWARDED_COUNT (production)
Set this to however many number of proxies you have running before your Meteor 
application. For example, if have an NGINX server acting as a proxy before your 
Meteor application, you would set HTTP_FORWARDED_COUNT=1. If you have a load 
balancer in front of that NGINX server, the count is 2.

MAIL_URL (development, production)
If you’re using an external mail service like Postmark, Mandrill, MailGun or 
SendGrid, you can provide a SMTP URL for your Meteor app to use to send e-mail. 
For example: MAIL_URL="smtp://user@pass:yourservice.com:587".

METEOR_SETTINGS (production)
When running your bundled application in production mode, pass a string of JSON 
containing your settings with 
METEOR_SETTINGS='{ "server_only_setting": "foo", "public": { "client_and_server_setting": "bar" } }'.
In development, this is accomplished with meteor --settings [file.json] in order to 
provide full-reactivity when changing settings. Those settings are simply passed as 
a string here. Please see the Meteor.settings documentation for further information.

MONGO_OPLOG_URL (development, production)
MongoDB server oplog URL. If you’re using a replica set (which you should), construct
this url like so: 
MONGO_URL="mongodb://user@password:myserver.com:10139/local?replicaSet=(your replica set)&authSource=(your auth source)"

MONGO_URL (development, production)
MongoDB server URL. Give a fully qualified URL (or comma-separated list of URLs) 
like MONGO_URL="mongodb://user@password:myserver.com:10139". For more information see the MongoDB docs.

METEOR_PACKAGE_DIRS (development, production)
Colon-delimited list of local package directories to look in, outside your normal 
application structure, for example: METEOR_PACKAGE_DIRS="/usr/local/my_packages/". 
Note that this used to be PACKAGE_DIRS but was changed in Meteor 1.4.2.

PORT (production)
Which port the app should listen on, for example: PORT=3030. See also: BIND_IP.
In development, this can be accomplished with meteor run --port <port>.

ROOT_URL (development, production)
Used to generate URLs to your application by, among others, the accounts package. 
Provide a full URL to your application like this: ROOT_URL="https://www.myapp.com".







