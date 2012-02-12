Return to Castle Wolfenstein multiplayer GPL source release
===========================================================

This file contains the following sections:

GENERAL NOTES
LICENSE

GENERAL NOTES
=============

Game data and patching:
-----------------------

This source release does not contain any game data, the game data is still
covered by the original EULA and must be obeyed as usual.

You must patch the game to the latest version.

Note that RTCW is available from the Steam store at
http://store.steampowered.com/app/9010/

Linux note: due to the game CD containing only a Windows version of the game,
you must install and update the game using WINE to get the game data.

Compiling on win32:
-------------------

A Visual C++ 2008 project is provided in src\wolf.sln.
The solution file is compatible with the Express release of Visual C++.

In order to test your binaries, backup and remove Main\mp_bin.pk3,
then replace WolfMP.exe, Main\qagame_mp_x86.dll, Main\cgame_mp_x86.dll, Main\ui_mp_x86.dll.
When starting the server make sure to specify Pure Server: No (sv_pure 0).

Compiling on GNU/Linux x86:
---------------------------

Go to the src/unix directory, and run the cons script
(cons was an old precursor to scons which we had been using in earlier projects)

Run ./cons -h to review build options. Use ./cons -- release to compile in release mode.

If any problems occur, consult the internet.

Other platforms, updated source code, security issues:
------------------------------------------------------

If you have obtained this source code several weeks after the time of release
(August 2010), it is likely that you can find modified and improved
versions of the engine in various open source projects across the internet.
Depending what is your interest with the source code, those may be a better
starting point.


LICENSE
=======

See COPYING.txt for the GNU GENERAL PUBLIC LICENSE
