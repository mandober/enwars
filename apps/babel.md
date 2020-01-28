# Babel

By default @babel/node cli and @babel/register will save to a json cache in your temporary directory. This will heavily improve with the startup and compilation of your files. There are however scenarios where you want to change this behaviour through the exposed enwars.

## BABEL_CACHE_PATH
- Specify different location for Babel's cache.
- https://babeljs.io/docs/usage/babel-register/
- e.g. BABEL_CACHE_PATH=/foo/my-cache.json babel-node script.js


## BABEL_DISABLE_CACHE
- Disable Babel's cache
- https://babeljs.io/docs/usage/babel-register/
- e.g. BABEL_DISABLE_CACHE=1 babel-node script.js
