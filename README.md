Étoilé 0.4.2
============

Étoilé intends to be an innovative GNUstep based user environnement built from
the ground up on highly modular and light components with project and document
orientation in mind, in order to allow users to create their own workflow by
reshaping or recombining provided Services (aka Applications), Components etc.
Flexibility and modularity on both User Interface and code level should allow us
to scale from PDA to computer environment.

Various licenses are used, they are specific to each module, but BSD and MIT
licenses are the most widely used. Apache, LGPL and even more rarely GPL
licenses are in used in few modules too.

Maintainers (core team): Quentin Mathe, Nicolas Roard, David Chisnall,
Jesse Ross, Yen-Ju Chen
Authors: Truls Becken, Isaiah Beerbower, Yen-Ju Chen, David Chisnall,
Michael Hanni, Jasper Hauser, Saso Kiselkov, Nyap Hong Koh, Uli Kusterer,
Manuel Guesdon, Quentin Mathe, Lennart Melzer, Guenther Noack, Nicolas Roard,
Jesse Ross, Eric Wasylishen,


To learn more about Étoilé:
<http://www.etoile-project.org>

**WARNING**: As it stands now, Étoilé is more or less a development environment and not a desktop environment. We have no working theme since we are still in the process of migrating from our Camaelon theme engine to the new one bundled with GNUstep. User-oriented applications such as Melodie can fail to launch or behave correctly because their development have been put on hold.


Build and Install
-----------------

Read the [install](INSTALL.md) documentation.


Mac OS X support
----------------

Various modules are compatible with Cocoa (Xcode project are usually included
but very often outdated, please submit back the ones you take time to update).

Here are modules with supported Cocoa compatibility:

* EtoileFoundation, EtoileThread, EtoileXML

* EtoileUI

* IconKit

* LuceneKit

* XMPPKit

* UnitKit


Maintained Modules
------------------

The Étoilé repository contains a large number of modules, but some of them have
no maintainer or might be deprecated in the near future. Here is a list of the
maintained modules, for which a long term support can be expected:

* BuildScripts

* Frameworks/
  * CoreObject
  * EtoileFoundation
  * EtoileText
  * EtoileUI
  * ScriptKit
  * SystemConfig
  * UnitKit
  * XMPPKit
  * Services/DocGenerator



* Developer/Services/ModelBuilder

* Languages/
  * LanguageKit
  * ParserKit
  * SourceCodeKit
  * Smalltalk


* Services/Private/
  * ObjectManager
  * System
  * ProjectManager
  * Worktable

The Etoile core frameworks are UnitKit, EtoileFoundation, CoreObject, LanguageKit,
SourceCodeKit, XMPPKit and EtoileUI.


Developer notes
===============

Tests suite
-----------

UnitKit (bundled with Étoilé) is required.

Steps to produce test bundles for every modules which supports it in the
repository and run tests suites:

* `make test=yes`

* `make check` (not yet implemented)


Dependency
----------

Unless you only build Cocoa compatible modules on Mac OS X, you have to install
GNUstep, this is the only mandatory dependency. To set up GNUstep with its
related dependencies, you should read about GNUstep install on
<http://www.gnustep.org>

* From GNUstep: `gnustep-make`, `gnustep-base`, `gnustep-gui`, `gnustep-back`

* From Freedesktop: D-Bus, HAL, startup-notification, Xcursor

* libpng, zlib, OniGuruma, XScreenSaver, LLVM, GMP, Lemon, SQLite,
  OSS, FFmpeg (libavcodec and libavformat), TagLib, MPEG4IP (libmp4v2),
  Graphviz, Discount

More details about Étoilé dependencies can be found in INSTALL document (in the
same directory than README one).


Contribute
----------

Read about [contributing](http://www.etoile-project.org/dev/contribute/) or
[hacking](HACKING.md) Étoilé.
