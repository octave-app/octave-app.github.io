# Octave.app Downloads

This page contains all the releases of Octave.app. If you're not sure which one to get, just grab the latest version, from the top of the page.

For betas and prereleases, including the new 5.x series see [Developer Downloads](/Developer-Downloads.html).

## Installation Notes

Our apps are not signed yet. This means that the first time you run them, you must right-click Octave.app and choose "Open" instead of just double-clicking it, and then choose "Run" from the dialog that pops up, when it asks you if you want to run an app from an "unkown developer".

We're working on fixing this by getting signed releases. Sorry for the inconvenience.

## Current Release

This is probably the one you want.

### Octave 6.2.0

Released April 16, 2021.

Requires macOS 10.14 or newer.

Download: [Octave-6.2.0.dmg](https://github.com/octave-app/octave-app/releases/download/v6.2.0/Octave-6.2.0.dmg)

Announcement: [Octave 6.2.0 Announcement](https://www.gnu.org/software/octave/news/release/2021/02/20/octave-6.2.0-released.html)

## Older Releases

You probably don't want these.

### Octave 6.1.0

Released Jan 22, 2021.

Requires macOS 10.13 or newer.

Download: [Octave-6.1.0.dmg](https://github.com/octave-app/octave-app/releases/download/v6.1.0/Octave-6.1.0.dmg)

Release Notes: [Octave 6.1.0 Release Notes](https://www.gnu.org/software/octave/NEWS-6.1.html)

### Octave 4.4.1 u1

Released Dec 2, 2019.

I forgot which versions of macOS it supports.

Download: [Octave-4.4.1.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.1-u1/Octave-4.4.1-u1.dmg)

Release Notes: [Octave 4.4.1 Release Notes](https://www.gnu.org/software/octave/news/release/2018/08/09/octave-4.4.1-released.html)

#### Known bugs

* Test suite may hang when run in GUI [Bug #21](https://github.com/octave-app/octave-app-bundler/issues/21)
* oct-files are not compatible with Octaves installed at different paths [Bug #43](https://github.com/octave-app/octave-app-bundler/issues/43)

### Octave 4.4.0

Released Dec 4, 2018.

Download: [Octave-4.4.0.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.0/Octave-4.4.0.dmg)

Release Notes: [Octave 4.4.0 Release Notes](https://www.gnu.org/software/octave/NEWS-4.4.html)

#### Java requirements

If you want Java to work inside Octave.app for Octave.app 4.4.0, you need to install a particular version of Java.

The Java 1.8 you have installed must be exactly `jdk1.8.0_181.jdk`, due to how the Octave build and Java detection system works. (This was the latest release of JDK 1.8 at the time Octave.app 4.4.0 was built.) You can download it [here](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).

If you do not care about Java working inside your Octave.app, you can ignore this JDK requirement entirely.

#### Known bugs

* Test suite may hang when run in GUI [Bug #21](https://github.com/octave-app/octave-app-bundler/issues/21)
* octfiles are not compatible with Octaves installed at different paths [Bug #43](https://github.com/octave-app/octave-app-bundler/issues/43)
