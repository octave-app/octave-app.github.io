Developer Downloads
====================

These are downloads for developers and testers of Octave.app. This page contains prerelease software that may be buggy.

If you are an Octave.app user, you probably want to go to our [main Download page](/Download.html) instead.

##  4.4.1 beta7

Beta 7 for Octave.app 4.4.1.

[Octave-4.4.1-beta7.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.1-beta7/Octave-4.4.1-beta7.dmg)

#### Changes

* Built against Oracle JDK 8u201 instead of 8u191.
* Octave.app build info is included in `ver` output.

##  4.4.1 beta5

Beta 5 for Octave.app 4.4.1.

[Octave-4.4.1-beta5.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.1-beta5/Octave-4.4.1-beta5.dmg)

This one is significant.

#### Changes

* Revert from our hacked Qt back to vanilla Qt in an effort to clear up some crashes and hangs related to saving files from the GUI file editor while you're stopped in them in the debugger.

##  4.4.1 beta4

Beta 4 for Octave.app 4.4.1.

[Octave-4.4.1-beta4.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.1-beta4/Octave-4.4.1-beta4.dmg)

#### Changes

* Fixes language support in the GUI
* Some dependency version bumps

##  4.4.1 beta3

Beta 3 for Octave.app 4.4.1.

[Octave-4.4.1-beta3.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.1-beta3/Octave-4.4.1-beta3.dmg)

#### Changes

* Fixes license info in VERSIONS file.

##  4.4.1 beta2

Beta for Octave.app 4.4.1.

[Octave-4.4.1-beta2.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.1-beta2/Octave-4.4.1-beta2.dmg)

#### Changes

* Adds custom `octave_app_diagnostic_dump` function.

##  4.4.1 beta1

First beta for 4.4.1.

[Octave-4.4.1-beta1.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.1-beta1/Octave-4.4.1-beta1.dmg)

##  4.4.0

Final release for Octave.app 4.4.0.

[Octave-4.4.0.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.0/Octave-4.4.0.dmg)

##  4.4.0 RC2

Release candidate for Octave.app 4.4.0.

[Octave-4.4.0-RC2.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.0-rc2/Octave-4.4.0-RC2.dmg)

This is the same as beta10, just re-labeled as a Release Candidate.

##  4.4.0-beta10

[Octave-4.4.0-beta10.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.0-beta10/Octave-4.4.0-beta10.dmg)

#### Changes

* Fixes the wrong-architecture build issue with RC1 and beta9.
* Build size size is back to normal.

##  4.4.0-beta9

[Octave-4.4.0-beta9.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.0-beta9/Octave-4.4.0-beta9.dmg)

#### Changes

* Fixes the Sundias/OpenBLAS dependency.
* OOPS: Introduces a regression in the build architecture.

##  4.4.0-beta8

Fixes the wrong-architecture build that causes crashes on older Macs.

[Octave-4.4.0-beta8.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.0-beta8/Octave-4.4.0-beta8.dmg)

##  4.4.0 RC1

Release candidate for Octave.app 4.4.0.

[Octave-4.4.0-rc1.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.0-rc1/Octave-4.4.0-rc1.dmg)

####  Changes

* [Test suite failures](https://github.com/octave-app/octave-app-bundler/issues/17) fixed.
* [Hacked Qt](https://github.com/octave-app/octave-app-bundler/issues/13) to avoid `FSEventStreamFlushSync(): failed assertion '(SInt64)last_id > 0LL'` messages
* VERSIONS now includes [source code links](https://github.com/octave-app/homebrew-octave-app/commit/1af9601aad55950276d1ebf78e9d10a46a72eb02) for all packages, for GPL compliance
* COPYING now [includes license info for all the dependency packages](https://github.com/octave-app/octave-app-bundler/issues/27)
* [Fixed Ghostscript initialization](https://github.com/octave-app/octave-app-bundler/issues/20)
* [Cairo terminal is enabled](https://github.com/octave-app/octave-app-bundler/issues/25)
* Cosmetic fixes

####  Known bugs

* [#33 Test failures during "make check"](https://github.com/octave-app/octave-app-bundler/issues/33)
* [#21 Intermittent hang during test suite in GUI](https://github.com/octave-app/octave-app-bundler/issues/21)
