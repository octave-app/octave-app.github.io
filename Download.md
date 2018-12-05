Octave.app Downloads
====================

This page contains all the releases of Octave.app. If you're not sure which one to get, just grab the latest version, from the top of the page.

## Installation Notes

Our apps are not signed yet. This means that the first time you run them, you must right-click Octave.app and choose "Open" instead of just double-clicking it, and then choose "Run" from the dialog that pops up, when it asks you if you want to run an app from an "unkown developer".

We're working on fixing this by getting signed releases. Sorry for the inconvenience.

##  Releases

###  Octave 4.4.0

Download: [Octave-4.4.0.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.0/Octave-4.4.0.dmg)

[4.4.0 Release Notes](https://www.gnu.org/software/octave/NEWS-4.4.html)

Java requirements:

The Java 1.8 you have installed must be exactly `jdk1.8.0_181.jdk`, due to how the Octave build and Java detection system works. (This was the latest release of JDK 1.8 at the time Octave.app 4.4.0 was built.) You can download it [here](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).

Known bugs:

* Test suite may hang when run in GUI [Bug #21](https://github.com/octave-app/octave-app-bundler/issues/21)
* octfiles are not compatible with Octaves installed at different paths [Bug #43](https://github.com/octave-app/octave-app-bundler/issues/43)
