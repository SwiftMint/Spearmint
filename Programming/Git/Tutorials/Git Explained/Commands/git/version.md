# `--version` | [git-version - Display version information about Git](https://git.github.io/htmldocs/git-version.html)
## `-v` <br> `--version` <br> `version`
---
```
git version 2.53.0.windows.2
```
---
```
$ git -v -h
usage: git version [--build-options]

    --[no-]build-options  also print build options
```
---
### `--build-options`
```
$ git -v --b
git version 2.53.0.windows.2
cpu: x86_64
built from commit: e9edee0b34751bf4d7d1feda0e2535bff64d4e77
sizeof-long: 4
sizeof-size_t: 8
shell-path: D:/git-sdk-64/usr/bin/sh
rust: disabled
feature: fsmonitor--daemon
gettext: enabled
libcurl: 8.18.0
OpenSSL: OpenSSL 3.5.5 27 Jan 2026
zlib: 1.3.1
SHA-1: SHA1_DC
SHA-256: SHA256_BLK
default-ref-format: files
default-hash: sha1
```
