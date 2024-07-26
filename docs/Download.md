# Octave.app Downloads

This page contains all the releases of Octave.app. If you're not sure which one to get, just grab the latest version, from the top of the page.

For betas and prereleases, see [Developer Downloads](/Developer-Downloads.html).

If you would like to receive notifications about new Octave.app releases, you can subscribe to the [Octave.app Announcements](https://github.com/octave-app/octave-app/issues/1) and [Octave.app Dev News](https://github.com/octave-app/octave-app/issues/289) issues on [the octave-app GitHub repo](https://github.com/octave-app/octave-app).

Since version 8.4.0, Octave.app has a native Apple Silicon build available. It's the one without the "-Intel" suffix on the installer file name. If you have a newer Mac, that's the one you want. (The Intel build will still run on Apple Silicon Macs, but it will be slower.)

## Installation Notes

Our apps are not signed yet. This means that the first time you run them, you must right-click Octave.app and choose "Open" instead of just double-clicking it, and then choose "Run" from the dialog that pops up, when it asks you if you want to run an app from an "unkown developer".

We're working on fixing this by making code-signed releases. Sorry for the inconvenience.

## IMPORTANT: Special Installation Instructions!

These installers require special installation steps, due to security measures in recent macOS releases.

Once you download the installer DMG file, and before opening it to do the installation, you must use `xattr` to clear the "quarantine" on it. To do this, open Terminal, and run the following:

```text
$ cd Downloads
$ xattr -c Octave-*.dmg
```

Then you can double-click the DMG file to open it and do the installation.

If you don't do this, then when you try to run Octave-8.4.0 from the Applications folder, you may get an error window saying "This app is damaged and should be moved to the trash" and it won't run.

Sorry for the inconvenience. I haven't figured out a better way to deal with this yet.

## Current Release

This is probably the one you want.

### Octave.app 9.2

Released July 25, 2024.

Requires macOS 12 or newer. (If it doesn't work on macOS 12 or 13, please let us know by [submitting a bug report](https://github.com/octave-app/octave-app/issues).)

NOTE: This requires a special extra step for installation, or the app will be broken. See the "Special Installation Instructions" section below!

#### Downloads

Downloads:

* [Octave-9.2.dmg](https://github.com/octave-app/octave-app/releases/download/v9.2/Octave-9.2.dmg) for Apple Silicon (M1, M2, M3) Macs
* [Octave-9.2-Intel.dmg](https://github.com/octave-app/octave-app/releases/download/v9.2/Octave-9.2-Intel.dmg) for older Intel Macs

Release page: [Octave.app 9.2 Release on GitHub](https://github.com/octave-app/octave-app/releases/tag/v9.2)

## Older Releases

You probably don't want these.

### Octave.app 9.1

Released July 25, 2024.

Requires macOS 12 or newer. (If it doesn't work on macOS 12 or 13, please let us know by [submitting a bug report](https://github.com/octave-app/octave-app/issues).)

NOTE: This requires a special extra step for installation, or the app will be broken. See the "Special Installation Instructions" section below!

#### Downloads

Downloads:

* [Octave-9.1.dmg](https://github.com/octave-app/octave-app/releases/download/v9.1/Octave-9.1.dmg) for Apple Silicon (M1, M2, M3) Macs
* [Octave-9.1-Intel.dmg](https://github.com/octave-app/octave-app/releases/download/v9.1/Octave-9.1-Intel.dmg) for older Intel Macs

Release page: [Octave.app 9.1 Release on GitHub](https://github.com/octave-app/octave-app/releases/tag/v9.1)

### Octave 8.4.0

Released May 3, 2024.

Requires macOS 12 or newer, possibly macOS 14 or newer. (If it doesn't work on macOS 12 or 13, please let us know by [submitting a bug report](https://github.com/octave-app/octave-app/issues).)

NOTE: This requires a special extra step for installation, or the app will be broken. See the "Special Installation Instructions" section below!

With this release, Octave.app now has a native Apple Silicon build available. It's the one without the "-Intel" suffix on the installer file name. If you have a newer Mac, that's the one you want.

#### Downloads

Downloads:

* [Octave-8.4.0.dmg](https://github.com/octave-app/octave-app/releases/download/v8.4.0/Octave-8.4.0.dmg) for Apple Silicon (M1, M2, M3) Macs
* [Octave-8.4.0-Intel.dmg](https://github.com/octave-app/octave-app/releases/download/v8.4.0/Octave-8.4.0-Intel.dmg) for older Intel Macs

Release page: [Octave.app 8.4.0 Release on GitHub](https://github.com/octave-app/octave-app/releases/tag/v8.4.0)

### Octave 6.2.0

Released April 16, 2021.

Requires macOS 10.14 or newer.

Download: [Octave-6.2.0.dmg](https://github.com/octave-app/octave-app/releases/download/v6.2.0/Octave-6.2.0.dmg)

Announcement: [Octave 6.2.0 Announcement](https://www.gnu.org/software/octave/news/release/2021/02/20/octave-6.2.0-released.html)

### Octave 4.4.1 u1

Released Dec 2, 2019.

I forgot which versions of macOS this supports; probably 10.13 and later.

Download: [Octave-4.4.1-u1.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.1-u1/Octave-4.4.1-u1.dmg)

Release Notes: [Octave 4.4.1 Release Notes](https://www.gnu.org/software/octave/news/release/2018/08/09/octave-4.4.1-released.html)

#### Known bugs

* Test suite may hang when run in GUI [Bug #21](https://github.com/octave-app/octave-app-bundler/issues/21)
* oct-files are not compatible with Octaves installed at different paths [Bug #43](https://github.com/octave-app/octave-app-bundler/issues/43)

### Octave 4.4.1

Released Feb 19, 2019.

I forgot which versions of macOS this supports; probably 10.13 and later.

Download: [Octave-4.4.1.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.1/Octave-4.4.1.dmg)

Release Notes: [Octave 4.4.1 Release Notes](https://www.gnu.org/software/octave/news/release/2018/08/09/octave-4.4.1-released.html)

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
