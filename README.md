# NXDK Packages

This repo contains the sources for a set of packages for the NXDK development kit for the original Xbox.

Changes to this repo are automatically build and hosted as a pacman repository.

# Using the repo

Make sure you have a pacman installation or pacman compatible program which is specifically set up for your local the NXDK installation. Anything else will destroy your system.

Here is an example of how to add this repository to `pacman.conf`:
```
[nxdk-packages]
SigLevel = Optional TrustAll
Server = https://github.com/sharkwouter/nxdk-packages/releases/latest/download/
```

After that running `pacman -Sy` and then `pacman -S $(pacman -Slq)` will install all packages from this repo.

# Contributing

If you wish to update or add a library take a look at the [contribution documentation](CONTRIBUTING.md).

## Licenses

To `PKGBUILD` files, scripts, documentation and GitHub related files in this repo the following license applies:

```
This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <https://unlicense.org>
```

Exceptions are patches and the packages resulting from this repository. Those take the licenses of the packaged software.
