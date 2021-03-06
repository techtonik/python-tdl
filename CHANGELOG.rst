===========
 Changelog
===========
1.3.1
 * Fixed pathfinding regressions.

1.3.0
 * Updated backend to use python-cffi instead of ctypes.  This gives decent
   boost to speed in CPython and a drastic to boost in speed in PyPy.

1.2.0
 * The set_colors method now changes the default colors used by the draw_*
   methods.  You can use Python's Ellipsis to explicitly select default colors
   this way.
 * Functions and Methods renamed to match Python's style-guide PEP 8, the old
   function names still exist and are depreciated.
 * The fgcolor and bgcolor parameters have been shortened to fg and bg

1.1.7
 * Noise generator now seeds properly
 * The OS event queue will now be handled during a call to tdl.flush. This
   prevents a common newbie programmer hang where events are handled
   infrequently during long animations, simulations, or early development
 * Fixed a major bug that would cause a crash in later versions of Python 3

1.1.6
 * Fixed a race condition when importing on some platforms
 * Fixed a type issue with quickFOV on Linux
 * Added a bresenham function to the tdl.map module

1.1.5
 * a for loop can iterate over all coordinates of a Console
 * drawStr can be configured to scroll or raise an error
 * You can now configure or disable key repeating with tdl.event.setKeyRepeat
 * Typewriter class removed, use a Window instance for the same functionality
 * setColors method fixed
 
1.1.4
 * Merged the Typewriter and MetaConsole classes,
   You now have a virtual cursor with Console and Window objects
 * Fixed the clear method on the Window class
 * Fixed screenshot function
 * Fixed some drawing operations with unchanging backgrounds
 * Instances of Console and Noise can be pickled and copied
 * Added KeyEvent.keychar
 * Fixed event.keyWait, and now converts window closed events into Alt+F4

1.1.3
 * Some of the setFont parameters were incorrectly labeled and documented
 * setFont can auto-detect tilesets if the font sizes are in the filenames
 * Added some X11 unicode tilesets, including unifont.

1.1.2
 * Window title now defaults to the running scripts filename
 * Fixed incorrect deltaTime for App.update
 * App will no longer call tdl.flush on its own, you'll need to call this yourself
 * tdl.noise module added
 * clear method now defaults to black on black

1.1.1
 * map submodule added with AStar class and quickFOV function
 * new Typewriter class
 * most console functions can use Python-style negative indexes now
 * new App.runOnce method
 * rectangle geometry is less strict

1.1.0
 * KeyEvent.keyname is now KeyEvent.key
 * MouseButtonEvent.button now behaves like KeyEvent.keyname does
 * event.App class added
 * drawing methods no longer have a default for the character parameter
 * KeyEvent.ctrl is now KeyEvent.control
