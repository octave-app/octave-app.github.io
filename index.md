Octave.app
==========

Octave.app is a project to bundle and distribute [GNU Octave](https://www.gnu.org/software/octave/) as a native Mac GUI application. This makes it easy to install and use GNU Octave on Mac.

We are not an official GNU project, or part of GNU Octave. We are a rag-tag band of misfits who've written a tool to download and build GNU Octave and its dependencies and bundle them as a Mac app.

Our goal is to make ready-to-use Octave.app installers available to the public.

## Download

All Octave.app releases are available on the [Downloads](/Download.html) page.

## Requirements

* macOS
* Java JDK 1.8 u171, if you want to use Java
* MacTeX, if you want the **info** command to work properly

The Java 1.8 you have installed must be exactly `jdk1.8.0_171.jdk`, due to how the Octave build and Java detection system works. This is the latest release of JDK 1.8. You can download it [here](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).

## License

Most of Octave.app's code is GPL, with the exception of its Homebrew formula files, which are BSD 2-Clause License.

GNU Octave itself is GPL. Its dependencies are available under various FLOSS licenses.

###  People

[Sebastian Schoeps](https://github.com/schoeps) is the original author and maintainer.

[Andrew Janke](https://apjanke.net) is a maintainer.
