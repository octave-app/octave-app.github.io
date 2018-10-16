Developer Downloads
====================

These are downloads for developers and testers of Octave.app. This page contains prerelease software that may be buggy.

If you are an Octave.app user, you probably want to go to our [main Download page](/Download.html) instead.

##  4.4.0-beta10

[Octave-4.4.0-beta10.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.0-beta10/Octave-4.4.0-beta10.dmg)

### Changes

* Fixes the wrong-architecture build issue with RC1 and beta9.
* Build size size is back to normal.

##  4.4.0-beta9

[Octave-4.4.0-beta9.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.0-beta9/Octave-4.4.0-beta9.dmg)

### Changes

* Fixes the Sundias/OpenBLAS dependency.
* OOPS: Introduces a regression in the build architecture.

##  4.4.0-beta8

Fixes the wrong-architecture build that causes crashes on older Macs.

[Octave-4.4.0-beta8.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.0-beta8/Octave-4.4.0-beta8.dmg)

##  4.4.0 RC1

Release candidate for Octave.app 4.4.0.

[Octave-4.4.0-rc1.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.0-rc1/Octave-4.4.0-rc1.dmg)

##  4.4.0-beta4

<strike>Code signing enabled! Now you can open the app by just double-clicking 
it.</strike> The code signing was broken.

[Octave-4.4.0-beta4.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.0-beta4/Octave-4.4.0-beta4.dmg)

##  4.4.0-beta3

Getting closer.

This one fixes a test failure in `make check` and gets rid of the double Dock icons.

[Octave-4.4.0-beta3.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.0-beta3/Octave-4.4.0-beta3.dmg)

##  4.4.0-beta2

This one might be ready for prime time! Test suite failures are all cleaned up now. -apjanke

[Octave-4.4.0-beta2.dmg](https://github.com/octave-app/octave-app/releases/download/untagged-4e9d0ab25492be932368/Octave-4.4.0-beta2.dmg)

###  Changes

* [Test suite failures](https://github.com/octave-app/octave-app-bundler/issues/17) fixed.
* [Hacked Qt](https://github.com/octave-app/octave-app-bundler/issues/13) to avoid `FSEventStreamFlushSync(): failed assertion '(SInt64)last_id > 0LL'` messages
* VERSIONS now includes [source code links](https://github.com/octave-app/homebrew-octave-app/commit/1af9601aad55950276d1ebf78e9d10a46a72eb02) for all packages, for GPL compliance
* COPYING now [includes license info for all the dependency packages](https://github.com/octave-app/octave-app-bundler/issues/27)
* [Fixed Ghostscript initialization](https://github.com/octave-app/octave-app-bundler/issues/20)
* [Cairo terminal is enabled](https://github.com/octave-app/octave-app-bundler/issues/25)
* Cosmetic fixes

###  Known bugs

* [#33 Test failures during "make check"](https://github.com/octave-app/octave-app-bundler/issues/33)
* [#21 Intermittent hang during test suite in GUI](https://github.com/octave-app/octave-app-bundler/issues/21)

##  4.4.0-beta1

Published Thu Jun 21 09:41:04 EDT 2018.

[Octave-4.4.0-beta1.dmg](https://github.com/octave-app/octave-app/releases/download/v4.4.0-beta1/Octave-4.4.0-beta1.dmg)

Known to have bugs: crashes during the test suite.
