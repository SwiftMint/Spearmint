# `--all` | Command List
##  `-a` <br> `--all`
### List all available commands.
```
$ git -h -a
See 'git help <command>' to read about a specific subcommand

Main Porcelain Commands
   add                     Add file contents to the index
   am                      Apply a series of patches from a mailbox
   archive                 Create an archive of files from a named tree
....
```
---
### `--no-external-commands`
#### Removes External Commands. <br> Output from `-a` typically includes these at the end:
```
External commands
   askpass
   askyesno
   credential-helper-selector
   credential-manager
   lfs
   update-git-for-windows
```
---
### `--no-aliases`
#### Removes aliases from `\~.gitconfig` (see `Aliasing (Bash + Git).md`) <br> Output from -a typically includes these after External Commands
```
Command aliases
   $                 $$
```
---
### `--verbose`
#### Describe each command in the list (Default). <br> `--no-verbose` will return only a list and identical output to `git` **/** `git -h` output.
```
$ git -h -a --no-v
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--no-lazy-fetch]
           [--no-optional-locks] [--no-advice] [--bare] [--git-dir=<path>]
           [--work-tree=<path>] [--namespace=<name>] [--config-env=<name>=<envvar>]
           <command> [<args>]

available git commands in 'C:/Program Files/Git/mingw64/libexec/git-core'

  add                       merge-one-file
  am                        merge-ours
  ....
```

See: `$$$$.md`
---