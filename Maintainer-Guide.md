Octave.app Maintainer's Guide
=============================

This document contains information for maintainers and developers of Octave.app. If you are an Octave.app user, you should not have to know or worry about anything in this document.

# Building Octave.app

## Requirements

* macOS
  * TODO: Determine which version we're going to build under. Should probably be an older one for back-compatibility.
* Xcode (needed for DMG creation)
* MacTeX (needed for document creation)
* Java 1.8 JDK u171

## Process

To build a distribution of Octave.app:

* Install Homebrew on your machine in the default prefix.
  * (This is necessary to get some external tools.)
* Clone the `octave-app/octave-app-bundler` repo.
  * `git clone https://github.com/octave-app/octave-app-bundler --recursive`
  * You must do `--recursive` to pick up required submodules.
* Delete any installed `/Applications/Octave.app` you might have.
* Run `./bundle_octave` inside the repo.

By default, `bundle_octave` will build default variant with the latest version of Octave.

See `./bundle_octave --help` for more options.

### Building a variant

Octave.app defines "variants" of the Octave build. These are builds that vary in their build options, the dependencies they are built with, or other aspects. For example, if we decide to support an OpenBLAS Octave build, that will be an "openblas" variant.

Some variants are for public consumption, and some are for internal debugging use.

Use the `-a`/`--variant` option of `bundle_octave` to build a variant.

Each variant is defined in a formula named `octave-<variant>` (possibly with versioned formulae named `octave-<variant>@<version>`). The variant name is included in the name of the built application.

Defined variants:

  * `unversioned` - uses unversioned formulae for `octave` and all its dependencies. This is for internal debugging use, and not for public distribution.

### Building a different version

To build a different version of Octave, use the `-V`/`--octave-version` to select the version of Octave to build. This version must be defined in an `octave[-<variant>]@<version>` formula.

### Single-threaded builds for debugging

If you want to do your compilations single-threaded, which will be slower but produce more readable output, set the environment variable HOMEBREW_MAKE_JOBS=1 before running bundle_octave.

You don't want to do this normally, because it will be _slow_, but it's useful in hunting down error messages from faild big builds like `gcc`.

# Making a distribution

To make a distribution, build Octave.app as described above. Then test your built application following the [docs/Testing-Script.md](https://github.com/octave-app/octave-app-bundler/blob/master/docs/Testing-Script.md) found in the `octave-app-bundler` repo.

# Tools

##  Custom brew commands

The `octave-app/octave-app` Homebrew tap defines some custom commands that are used for maintaining the formulae that go in to an Octave.app build.

###  octave-app-grab

This "grabs" copies of formulae from `homebrew-core` or wherever they are defined and creates versioned variants of them in the `octave-app/octave-app` tap on the local machine. The formulae themselves are versioned, and all their dependencies are also frozen at the current version.

Run `brew octave-app-grab --deps` to grab all the dependencies of `octave` (or some other named formula) and freeze all their versions. For manual fixups of individual formulae, you can also run `brew octave-app-grab <formula>`.

After the formula are grabbed, they need to be committed and pushed, so that `bundle_octave` can pick them up in the `octave-app/octave-app` tap that it has tapped in the app staging directory.

###  deps-with-versions

This is an informational command that lists a formula's dependencies which are versioned formulae. This can be useful in diagnosing problems with version freezing.

Examples:

```
$ brew deps-with-versions octave
$ brew deps-with-versions octave@4.4.0
automake@1.16.1
gnu-sed@4.5
pkg-config@0.29.2
libtool@2.4.6
veclibfort@0.4.2
...
$ brew deps-with-versions zim
python@2
```

The plain `octave` run produces nothing as output; this is expected, because the unversioned `octave` formula does not have versioned dependencies.

## create-dmg

We maintain our own fork of `create-dmg` at [octave-app/create-dmg](https://github.com/octave-app/create-dmg). It contains enhancements that we use in creating our installer DMG. It is included as a submodule in `octave-app-bundler`, so you don't need to fetch it separately.

#  Formula customizations

We use several customized formulae for building Octave. The base variants of the customized formulae are located in [octave-app/homebrew-octave-app-versions](https://github.com/octave-app/homebrew-octave-app-versions). (They are then grabbed by `brew octave-app-grab` into `homebrew-octave-app`.)

We customize the following formulae. This means that once a versioned formula is created, it needs to be hand-tweaked by a maintainer, and then cannot be regenerated from the base formula.

* `gnuplot`
  * Make `--with-cairo --with-qt` the defaults.
* `qt`
  * Patch it to remove FSEventStreamFlushSync calls, to avoid assertion failure warnings that show up in the GUI.
* `qscintilla2`
  * Make `--without-python --without-python2 --without-plugin` the defaults.
    * As of June 2018 `--without-plugin` is already the default in the current `qscintilla2` formula in `homebrew-core`. This can probably be removed.
  * Make the `pyqt` and `sip` dependencies conditional on Python usage.
    * This allows us to build a Python-free Octave.
* `gnu-tar`
  * Install with default name `tar`, no `gtar` prefix.

#  Defining a variant

To define a new variant, create an `octave-<variant>.rb` formula in `homebrew-octave-app-bases`. Then run `brew octave-app-grab octave-<variant>` to freeze it to a particular set of versions.

You can also skip the first step, and manually create an `octave-<variant>@<version>.rb` formula in `homebrew-octave-app`.

# Style Guide

## Prose style

The product name is "Octave.app". It is styled in proportional font.

The specific produced programs are "`Octave-<version>.app`". They are styled in fixed-width font.

Use Oxford commas.

## Code style

Ruby code: follow the Homebrew style guidelines.

Shell code: indent with two spaces, not tabs.
