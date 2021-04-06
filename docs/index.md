# Octave.app

Octave.app is a project to bundle and distribute [GNU Octave](https://www.gnu.org/software/octave/) as a native Mac GUI application. This makes it easy to install and use GNU Octave on Mac.

We are not an official GNU project, or part of GNU Octave. We are a rag-tag band of misfits who've written a tool to download and build GNU Octave and its dependencies and bundle them as a Mac app.

Our goal is to make ready-to-use Octave.app installers available to the public.

## Download

All Octave.app releases are available on the [Downloads](/Download.html) page.

When running Octave.app for the first time, instead of just double-clicking it, you will need to right-click on it and choose "Open", so you get a dialog asking you if you really want to run it, since it's from an unidentified developer. This is because the app is not signed. This is something we're working on.

If you're feeling adventurous, beta and pre-release versions can be found on the [Developer Downloads](/Developer-Downloads.html) page.

## Requirements

* macOS, version 10.11 El Capitan or newer
* MacTeX, if you want the **help** command to work properly for Octave Forge packages.

## License

Most of Octave.app's code is GPL, with the exception of its Homebrew formula files, which are BSD 2-Clause License.

GNU Octave itself is GPL. Its dependencies are available under various FLOSS licenses.

## Alternate Installations

### Installing with Homebrew Cask

To install Octave.app using Homebrew Cask:

```bash
brew tap octave-app/octave-app
brew install --cask octave-app
```

### Installing directly with Homebrew

NOTE: This is not the normal way to install Octave.app! Unless you have a particular reason for doing this, please just [download and install the regular Octave.app distribution](/Download.html).

If you want to build and install our Qt-enabled Octave build via Homebrew instead of using the Octave.app distribution, you can do this by setting up Homebrew as normal, and doing the following:

```bash
brew tap octave-app/octave-app-bases
brew install octave-octave-app
```

If you have a previous `octave` build from the regular Homebrew or [dpo/openblas](https://github.com/dpo/homebrew-openblas) formulae, you need to unlink it first with `brew unlink octave`.

## People and Support

[Sebastian Schoeps](https://github.com/schoeps) is the original author and maintainer.

[Andrew Janke](https://apjanke.net) is a maintainer.

For help with Octave.app, please head to the [octave-app GitHub repo](https://github.com/octave-app/octave-app) and see its issue tracker. Andrew also sometimes hangs out on the `#octave` channel on [freenode IRC](https://freenode.net/).

## Acknowledgements

Octave.app is powered by [Homebrew](https://brew.sh). ![Homebrew logo](images/homebrew-128x128.png)
