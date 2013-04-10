rssowl-portable
===============

A portable version of RSSOwl. This repository should contain build scripts and configuration files to modify RSSOwl from https://github.com/rssowl/RSSOwl to be portable.

See
---
* https://sourceforge.net/p/rssowl/discussion/296910/thread/696dafff/
* https://sourceforge.net/p/rssowl/discussion/296910/thread/57483982/

further info
------------
* http://portableapps.com/development
* http://portableapps.com/manuals/PortableApps.comLauncher/ref/index.html
* older RSSOwl portable link:
  * http://portableapps.com/node/19271 RSSOwl 2M9 Portable Dev Test 4
  * http://portableapps.com/node/24728 RSSOwl Portable 2.0.6 Development Test1
  * http://code.google.com/p/rssowl-portable/ (of RSSOwl 1.2.3 version)
  * http://portableapps.com/search/node/RSSOwl

TODO
----
* add documentation
* add scripts to auto-generate RSSOwl.ini, PortableApps.com installer, …
* include translations
* discuss (and write docs) whether RSSOwl portable should
	* be shipped with all available translations
	* be shipped in ~20 versions, one for each translation
* discuss (and write docs) whether RSSOwl portable should
	* disable auto-update and update via PortableApps.com platform
	* enable auto-update and not update via PortableApps.com platform

BUILDING
--------
How to generate a RSSOwlPortable.paf.exe installer:
1) Download the Windows zip file of RSSOwl from http://www.rssowl.org/download
2) extract its contents to /Portableapps.com/RSSOwlPortable/App/RSSOwl
3) Run PortableApps.com Launcher (generates the RSSOwlPortable Launcher)
4) Run PortableApps.com Installer (generates the RSSOwlPortable.paf.exe installer

Debugging
---------
* for debugging the installer see http://portableapps.com/manuals/PortableApps.comLauncher/advanced/debug.html
* for debugging RSSOwl see http://www.rssowl.org/help , the forum and the source code repository
