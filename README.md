fast c-string transformations

[![Build Status](https://travis-ci.org/client9/stringencoders.svg?branch=master)](https://travis-ci.org/client9/stringencoders)

Hello!

I don't use this library anymore and try to avoid C programming at all costs.  That said,
I'm very happy to accept pull-requests and collaborators.

## Install from Source

* You'll need to install autoconf, automake and libtool
* run `./bootstrap.sh`
* run `./configure`
* run `make && make check`

## Known Issues:

* `modp_base64_decode` expects **aligned** strings as input.  For Intel, is
  doesn't matter.  But for ARM chips it can segfault.
* `modp_numtoa.c` functions may produce different rounding than whatever
  `printf` is on your system. 

## Alpine Linux / musl-libc

* As mentioned, the tests for `modp_numtoa.c`  may fail due to different
  rounding algorithm.
* https://wiki.alpinelinux.org/wiki/How_to_get_regular_stuff_working
* `apk add gcc bash autoconf automake libtools util-linux pciutils usbutils coreutils binutils findutils grep`

