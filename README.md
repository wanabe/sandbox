# sandbox

This software provides sandbox environments with docker-compose / vagrant.

## install

```
$ git clone https://github.com/wanabe/sandbox.git
$ cd sandbox
$ ./sandbox --install
```

Then you can get ~/.local/bin/sandbox as symbolic link.

## usage

```
sandbox [ -v /path/of/host/:/path/of/env[;opt1=val1;opt2=val2] ] sandbox-name
```

Options of volume are only for vagrant.

### examples

```
$ sandbox -v ~/work/prog/ruby/ruby:/ruby';type="rsync";rsync__exclude="tmp"' openbsd6
```

Above means it runs openbsd6 sandbox with shared directory "~/work/prog/ruby/ruby" excludes "~/work/prog/ruby/ruby/tmp".

```
$ USER=wanabe sandbox -v ~/work/prog/ruby/ruby:/ruby ppc64le/ruby
```

Above means it runs ppc64le/ruby with shared directory "~/work/prog/ruby/ruby" as user "wanabe".

## current list of sandboxes

* aarch64
  * aarch64/ruby
* alpine
  * alpine/ruby
* mingw-w64-x86-64
  * mingw-w64-x86-64/ruby
* openbsd6
* openindiana
* ppc64le
  * ppc64le/ruby
* ubuntu
  * ubuntu/ruby

You can also get the list with `-l` or `-L` option.

```
$ sandbox -l
aarch64
aarch64/ruby
alpine
alpine/ruby
mingw-w64-x86-64
mingw-w64-x86-64/ruby
openbsd6
openindiana
ppc64le
ppc64le/ruby
ubuntu
ubuntu/ruby

$ sandbox -L
* aarch64
  * aarch64/ruby
* alpine
  * alpine/ruby
* mingw-w64-x86-64
  * mingw-w64-x86-64/ruby
* openbsd6
* openindiana
* ppc64le
  * ppc64le/ruby
* ubuntu
  * ubuntu/ruby
```
