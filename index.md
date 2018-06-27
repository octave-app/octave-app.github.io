Octave.app
==========

Octave.app is a project to bundle and distribute [GNU Octave](https://www.gnu.org/software/octave/) as a native Mac GUI application. This makes it easy to install and use GNU Octave on Mac.

We are not an official GNU project, or part of GNU Octave. We are a rag-tag band of misfits who've written a tool to download and build GNU Octave and its dependencies and bundle them as a Mac app.

Our goal is to make ready-to-use Octave.app installers available to the public.

## Download

All Octave.app releases are available on the [Downloads](/Download.html) page.

When running Octave.app for the first time, instead of just double-clicking it, you will need to right-click on it and choose "Open", so you get a dialog asking you if you really want to run it, since it's from an unidentified developer. This is because the app is not signed. This is something we're working on.

## Requirements

* macOS
* Java JDK 1.8 u171, if you want to use Java
* MacTeX, if you want the **info** command to work properly

The Java 1.8 you have installed must be exactly `jdk1.8.0_171.jdk`, due to how the Octave build and Java detection system works. This is the latest release of JDK 1.8. You can download it [here](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).

## License

Most of Octave.app's code is GPL, with the exception of its Homebrew formula files, which are BSD 2-Clause License.

GNU Octave itself is GPL. Its dependencies are available under various FLOSS licenses.

## Alternate Installations

### Installing with Homebrew Cask

To install Octave.app using Homebrew Cask:

```
brew tap octave-app/octave-app
brew cask install octave-app
```

### Installing directly with Homebrew

NOTE: This is not the normal way to install Octave.app! Unless you have a particular reason for doing this, please just [download and install the regular Octave.app distribution](/Download.html).

If you want to build and install our Qt-enabled Octave build via Homebrew instead of using the Octave.app distribution, you can do this by setting up Homebrew as normal, and doing the following:

```
brew tap octave-app/octave-app-bases
brew install octave-octave-app
```

If you have a previous `octave` build from the regular Homebrew or [dpo/openblas](https://github.com/dpo/homebrew-openblas) formulae, you need to unlink it first with `brew unlink octave`.

###  People

[Sebastian Schoeps](https://github.com/schoeps) is the original author and maintainer.

[Andrew Janke](https://apjanke.net) is a maintainer.
