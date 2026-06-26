# [Bash Built-in Commands](https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html#Bash-Builtin-Commands)
## [alias](https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html#Aliases)
```
alias [-p] [name[=value] ...]
```
`alias` or `alias -p`(rint) return a list of all aliases.

Baseline aliases are as follows:
```
alias ll='ls -l'
alias ls='ls -F --color=auto --show-control-chars'
alias winget='winpty winget.exe'
```
You cannot include any of the following characters in an alias name:
- **`/`** (Slash)
- `$` (Dollar Sign)
- **`'`** (Apostrophe)
- `=` (Equal Sign)

### In Bash, NOT in Git | Must re-do everytime [Aliases]:
```
help="git help"
g=git
gvr="git -v"
gvrlong="git version --build-options"
cl=clear
```

## unalias
```
unalias [-a] name[ ...]
```
`unalias -a`(ll) removes all aliases.

## For GIT Aliases:
```
git config --global alias.$$ "$$$ $$$"
```
+
```
git config --global alias
```
### OR
Edit the `~/.gitconfig:` file.
```
[alias]
      $$ = $$$$$
```

---