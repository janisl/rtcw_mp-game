Return to Castle Wolfenstein multiplayer GPL game source
========================================================

This file contains the following sections:

GENERAL NOTES
LICENSE

GENERAL NOTES
=============

Game engine:
------------

This release contains only the source of the game DLL files. It was separated
from JLQuake in order to keep it clean and because there are no plans on doing
any improvements on game code. 32 bit game DLLs built from this release should
still be compatible with original engine, but it's recomended to use an improved
game engine such as JLQuake.

Game data and patching:
-----------------------

This source release does not contain any game data, the game data is still
covered by the original EULA and must be obeyed as usual.

You must patch the game to the latest version.

Note that RTCW is available from the Steam store at
http://store.steampowered.com/app/9010/

Linux note: due to the game CD containing only a Windows version of the game,
you must install and update the game using WINE to get the game data.

Compiling on Windows:
-------------------

A Visual C++ 2010 project is provided in src\wolf.sln.
The solution file is compatible with the Express release of Visual C++.

In order to test your 32 bit binaries, backup and remove Main\mp_bin.pk3,
then replace Main\qagame_mp_x86.dll, Main\cgame_mp_x86.dll, Main\ui_mp_x86.dll.

On 64 bit Windows copy files qagame_mp_x86_64.dll, cgame_mp_x86_64.dll
and ui_mp_x86_64.dll into Main directory on RTCW install. You'll need a 64 bit
version of JLQuake to run them.

When starting the server make sure to specify Pure Server: No (sv_pure 0).

Compiling on GNU/Linux and other UNIX based systems:
----------------------------------------------------

mkdir build
cd build
cmake ..
make

You can test your 32 bit binaries by replacing qagame.mp.i386.so,
cgame.mp.i386.so, ui.mp.i386.so in directory main of the RTCW install.

On 64 bit systems copy qagame.mp.x86_64.so, cgame.mp.x86_64.so and
ui.mp.x86_64.so into directory main of the RTCW install. You'll need a 64 bit
version of JLQuake to run them.

When starting the server make sure to specify Pure Server: No (sv_pure 0).


LICENSE
=======

See COPYING.txt for the GNU GENERAL PUBLIC LICENSE
