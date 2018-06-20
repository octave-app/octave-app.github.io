Octave.app Maintainer's Guide
=============================

This document contains information for maintainers and developers of Octave.app. If you are an Octave.app user, you should not have to know or worry about anything in this document.

# Building Octave.app

To build a distribution of Octave.app:

* Install Homebrew on your machine in the default prefix.
  * (This is necessary to get some external tools.)
* Clone the `octave-app/octave-app-bundler` repo, recursively.
  * `git clone https://github.com/octave-app/octave-app-bundler --recursive`
* Delete any installed `/Applications/Octave.app` you might have.
* Run `./bundle_octave` inside the repo.

See `./bundle_octave --help` for more options. You might want to use:

  * `-f`/`--octave-formula` to use an alternate Octave.app Octave formula, such as `octave-unversioned`. (Build variants like OpenBLAS and CLI-only will also go here, probably.)
  * `-u`/`--build-suffix` to do a special release, such as a prerelease or a patch.
  * `-V`/`--octave-version` to select the version of Octave to build. This requires the version-specific of `octave` (or whatever you specified with `-f`) to exist, and be committed to `homebrew-octave-app`.


### Single-threaded builds for debugging

If you want to do your compilations single-threaded, which will be slower but produce more readable output, set the environment variable HOMEBREW_MAKE_JOBS=1 before running bundle_octave.

You don't want to do this normally, because it will be _slow_, but it's useful in hunting down error messages from faild big builds like `gcc`.

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

##  Formula customizations

We customize the following formulae. This means that once a versioned formula is created, it needs to be hand-tweaked by a maintainer, and then cannot be regenerated from the base formula.

* `gnuplot`
  * Make `--with-cairo --with-qt` the defaults.
* `qscintilla2`
  * Make `--without-python --without-plugin` the defaults.
    * TODO: That `--without-python` just turns off Python 3 bindings. Can we also turn off Python 2 bindings?
    * As of June 2018 `--without-plugin` is already the default in the current `qscintilla2` formula in `homebrew-core`. This can probably be removed.
* `cmake`
  * Make the `sphinx-doc` dependency unconditional
    * This is because it's not being picked up properly by `brew` when you do `brew install octave` and `cmake` gets picked up as a recursive dependency. Looks like a `brew` dependency resolution bug.



# Style Guide

## Prose style

The product name is "Octave.app". It is styled in proportional font.

The specific produced programs are "`Octave-<version>.app`". They are styled in fixed-width font.

Use Oxford commas.

## Code style

Ruby code: follow the Homebrew style guidelines.

Shell code: indent with two spaces, not tabs.
