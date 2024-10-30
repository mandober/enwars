# Zsh

In zsh, uppercased enwars are scalars and lowercased ones are arrays.

Var with the same name but different case are **connected variables**: uppercased var (e.g. `PATH`) is the traditional string-like var, and the lowercase (e.g. `path`) is its array representation. These are connected pairs - changing one changes the other. There are many connected var pairs where the changes made to one are automatically reflected on the other.

ZBEEP
ZDOTDIR
zle_bracketed_paste
zle_highlight
ZLE_LINE_ABORTED
ZLE_REMOVE_SUFFIX_CHARS
ZLE_RPROMPT_INDENT
ZLE_SPACE_SUFFIX_CHARS
ZSH_EVAL_CONTEXT
ZSH_NAME
ZSH_PATCHLEVEL
ZSH_SUBSHELL
ZSH_VERSION

connected var pairs:
- PATH and path
