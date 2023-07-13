# Contributing

This repository contains the build scripts for libraries for the NXDK. If you feel any library is missing or could use an update, let us know or feel free to submit a pull request.

## How to add a library

An ``NXBUILD`` file is actually a ``PKGBUILD`` like you might know them from Arch Linux, which means the Arch wiki is a great resource for how to write. Take a look [here](https://wiki.archlinux.org/title/Creating_packages) and [here](https://wiki.archlinux.org/title/PKGBUILD).

Start by creating a directory for the library and an ``NXBUILD`` file. It is recommended to base it on another ``NXBUILD`` in this repo which uses the same build system as the new library. Do make sure pkgname, pkgdesc, pkgver and license are changed, though.

Before making a pull request, make sure the library builds, installs and works.

Also make sure to read the criteria for contributions below.

## Criteria for contributions

For new contributions to be merged, the NXBUILDs in them should meet the following criteria:

- For new packages:
  - The following optional fields should not be forgotten:
    - `pkgdesc`
    - `license`
    - `url`
    - ``arch`` should be set to ``('x86')``.
    - ``sha256sums`` should be used for integrity checks of downloaded files. Git sources are allowed to use `SKIP`.
  - NXBUILDs based on versioned archive files (yourlibrary-1.2.tar.gz for instance) are preferred over those based on git/svn repositories.
  - The license of the library has to be installed in ``$pkgdir/psp/share/licenses/$pkgname/``.
  - NXBUILDs which use a git repository as source have to specify a tag or commit.
  - ``pkgname`` should not contain capital letters or special characters other than ``-``.
- For existing packages:
  - Either the ``pkgver`` or ``rel`` has been changed.
- For all NXBUILDs:
  - Libraries go in ``$pkgdir/psp/lib/``.
  - Include files go in ``$pkgdir/psp/include/``.
  - Pkgconfig files go in ``$pkgdir/psp/lib/pkgconfig``.
  - License files go in ``$pkgdir/psp/share/licenses/$pkgname/``.
  - Scripts which should be in the path of the user go in ``$pkgdir/bin/``.
  - Other scripts go in ``$pkgdir/psp/bin/`` or ``$pspdir/share/$pkgname/bin/``.
  - Documentation goes in ``$pkgdir/psp/share/doc/$pkgname/`` or ``$pkgdir/share/doc/$pkgname/``.
