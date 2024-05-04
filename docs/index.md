# Octave.app

Octave.app is a project to bundle and distribute [GNU Octave](https://www.gnu.org/software/octave/) as a native Mac GUI application. This makes it easy to install and use GNU Octave on Mac.

We are not an official GNU project, or part of GNU Octave. We are a rag-tag band of misfits who've written a tool to download and build GNU Octave and its dependencies and bundle them as a Mac app.

Our goal is to make ready-to-use Octave.app installers available to the public.

## Download

### TL;DR

[Click here](https://github.com/octave-app/octave-app/releases/download/v8.4.0/Octave-8.4.0.dmg) to get Octave.app 8.4.0, the latest release. (Or [click here](https://github.com/octave-app/octave-app/releases/download/v8.4.0/Octave-8.4.0-Intel.dmg) if you're using an older Intel-based Mac.)

Then do `xattr -c` on the downloaded file, and then open it and drag `Octave-8.4.0` to `Applications` to install it.

#### IMPORTANT: Special Installation Instructions!

These installers require special installation steps, due to security measures in recent macOS releases.

Once you download the installer DMG file, and before opening it to do the installation, you must use `xattr` to clear the "quarantine" on it. To do this, open Terminal, and run the following:

```text
$ cd Downloads
$ xattr -c Octave-*.dmg
```

Then you can double-click the DMG file to open it and do the installation.

If you don't do this, then when you try to run Octave-8.4.0 from the Applications folder, you may get an error window saying "This app is damaged and should be moved to the trash" and it won't run.

Sorry for the inconvenience. I haven't figured out a better way to deal with this yet.

Details on the release page: [Octave.app 8.4.0 release](https://github.com/octave-app/octave-app/releases/tag/v8.4.0).

### Details

All Octave.app releases are available on the [Downloads](/Download.html) page.

When running Octave.app for the first time, instead of just double-clicking it, you will need to right-click on it and choose "Open", so you get a dialog asking you if you really want to run it, since it's from an unidentified developer. This is because the app is not signed. This is something we're working on.

If you're feeling adventurous, some beta and pre-release versions can be found on the [Developer Downloads](/Developer-Downloads.html) page.

## Requirements

* macOS, version 12 Monterey or newer
  * (Some older versions of Octave.app support older versions of macOS.)
* MacTeX, if you want the **help** command to work properly for Octave Forge packages

## License

Most of Octave.app's code is GPL, with the exception of its Homebrew formula files, which are BSD 2-Clause License.

GNU Octave itself is GPL. Its dependencies are available under various FLOSS licenses. See the license files in the distribution for details.

## Alternate Installations

### Installing with Homebrew Cask

To install Octave.app using Homebrew Cask:

```bash
brew tap octave-app/octave-app
brew install --cask octave-app
```

You don't need to do it this way. This is only provided for people who like using Homebrew Casks instead of downloading a regular installer.

### Installing directly with Homebrew

NOTE: This is not the normal way to install Octave.app! Unless you have a particular reason for doing this, please just [download and install the regular Octave.app distribution](/Download.html) instead.

If you want to build and install our Qt-enabled Octave via Homebrew instead of using the Octave.app distribution, you can do this by setting up Homebrew as normal, and doing the following:

```bash
brew tap octave-app/octave-app
brew install octave-octapp
```

Then you can run it by calling `octave-octapp` (instead of plain `octave`).

## People, Support, and Source Code

[Sebastian Schoeps](https://github.com/schoeps) is the original author and maintainer.

[Andrew Janke](https://apjanke.net) is the current primary maintainer.

For help with Octave.app, please head to the [octave-app GitHub repo](https://github.com/octave-app/octave-app) and see its issue tracker. Andrew also sometimes hangs out on the [GNU Octave Discourse](https://octave.discourse.group/).

The full code for all the projects associated with Octave.app is in the [octave-app organization on GitHub](https://github.com/octave-app). The major parts are:

* [octave-app](https://github.com/octave-app/octave-app), which publishes the Octave.app distribution itself.
* [octave-app-bundler](https://github.com/octave-app/octave-app-bundler), the tool that builds Octave.app from its sources and dependencies.
* [homebrew-octave-app](https://github.com/octave-app/homebrew-octave-app), a [Homebrew Tap](https://docs.brew.sh/Taps) that holds the formulae for building the custom Octave.app-specific versions of its dependencies.

## Acknowledgments

Octave.app is powered by [Homebrew](https://brew.sh). Its entire build structure is built on Homebrew!

![Homebrew logo](images/homebrew-128x128.png)

Octave.app's M1 build server is provided by [MacStadium](https://www.macstadium.com/).

![MacStadium Developer Logo](images/MacStadium-developerlogo-abitsmaller.png)
