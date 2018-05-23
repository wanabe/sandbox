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
$ sandbox -v ~/work/prog/ruby/ruby:/ruby';type="rsync";rsync__exclude="tmp"' vagrant/openbsd6
```

Above means it runs vagrant/openbsd6 sandbox with shared directory "~/work/prog/ruby/ruby" excludes "~/work/prog/ruby/ruby/tmp".

```
$ USER=wanabe sandbox -v ~/work/prog/ruby/ruby:/ruby docker/ppc64le/ruby
```

Above means it runs docker/ppc64le/ruby with shared directory "~/work/prog/ruby/ruby" as user "wanabe".

## current list of sandboxes

* docker
  * docker/ubuntu
    * docker/ubuntu/ruby
  * docker/ppc64le
    * docker/ppc64le/ruby
  * docker/aarch64
    * docker/aarch64/ruby
  * docker/alpine
    * docker/alpine/ruby
  * docker/mingw-w64-x86-64
    * docker/mingw-w64-x86-64/ruby
* vagrant
  * vagrant/openindiana
  * vagrant/openbsd6

You can also get the list with `-l` or `-L` option.
