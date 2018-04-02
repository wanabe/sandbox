# sandbox

This software provides sandbox environments with docker-compose.

## install

```
$ git clone https://github.com/wanabe/sandbox.git
$ cd sandbox
$ ./sandbox --install
```

Then you can get ~/.local/bin/sandbox as symbolic link.

## usage

```
sandbox [ -v /path/of/host/:/path/of/env ] sandbox-name
```

## current list of sandboxes

* mingw-w64-x86-64
  * mingw-w64-x86-64/ruby
* ppc64le
  * ppc64le/ruby

You can also get the list with `-l` option.

```
$ envset -l
mingw-w64-x86-64
ppc64le
```
