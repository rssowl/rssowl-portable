This document lists all test cases to be checked before RSSOwlPortable is being released to public. For all test cases listed here you need to make sure that there is no RSSOwl installed on the local host.


1 Find Java Runtime
===================
What is being tested:
---------------------
* RSSOwlPortable should find a Java Installation to run using the '-vm %JAVA_HOME%\bin' argument provided by PortableApps.com Launcher
* RSSOwlPortable should use a working Java installation
* If no Java Installation could be found, try to rely on Java installed on the host operating system
* If finding Java fails a useful error message should be displayed

Possible setups:
----------------
A) 32Bit Java installed on host operating system
B) 64Bit Java installed on host operating system
C) 32Bit Java in PortableApps.com Suite (via jPortable package)
D) 64Bit Java in PortableApps.com Suite (via jPortable 64 package)
(Note that you need to make sure that no other Java Runtime is available)

Conditions to pass this test:
-----------------------------
1. If neither of A, B, C, D are present, RSSOwlPortable should display a useful error message
2. If neither of C, D are present at installation of RSSOwlPortable should display a useful message to inform the user that RSSOwlPortable requires Java to be installed. This does not need to abort the installation.
3. On any combination of A, B, C, D RSSOwl should be able to start fine


2 Correctly resolve relative path variables
===========================================
What is being tested:
---------------------
* The correct use of the '-data %PAL:DataDir%' argument provided by PortableApps.com Launcher
* RSSOwls behavior for saving data
see Bug #2 for details: https://github.com/rssowl/rssowl-portable/issues/2

Possible setups:
----------------
A) RSSOwlPortable on thumb drive
B) RSSOwlPortable on local disk
C) RSSOwlPortable on folder within thumb drive

Setup:
------
1. Move RSSOwlPortable (the folder) to a random folder on local disk
2. make sure that only one single “installation” of RSSOwlPortable is available on the currently tested system
3. run RSSOwl, modify some data, add feeds, …
4. close RSSOwl (make sure to close, not minimize to tray)
5. check the error log (see http://www.rssowl.org/help#item_5 for details) on errors
6. move the RSSOwlPortable somewhere else, including
	* a thumb drive
	* a different folder on local disk
	* a different PC (with thumb drive)
	* a different PC (local disk)
	and repeat 3./4./5.

This test case is passed if RSSOwls data (Database, Preferences, Log files, …) is consistent
over all different locations it is being checked and there are no errors related
to moving the RSSOwlPortable folder.


3 Do not write non-portable data
================================
Test setup:
-----------
1. Start ProcessMonitor (procmon) from the Sysinternals suite, http://technet.microsoft.com/de-de/sysinternals/bb896645 (also available in PortableApps.com Suite)
2. use procmon to monitor everything related to RSSOwlPortable
3. start RSSOwlPortable, use it and exit it
4. check procmon logs
This test case is passed if RSSOwlPortable does not write to the registry or folders outside the RSSOwlPortable folder.


4 Run from paths with spaces in it
==================================
Test setup:
-----------
1. Install RSSOwlPortable to a path containing spaces
2. Run RSSOwlPortable

This test is passed if RSSOwlPortable runs fine in such case.


5 Language TODO
===============


See
===
* http://portableapps.com/manuals/PortableApps.comLauncher/topics/checklist.html (some of that is already covered by the listed test cases)
