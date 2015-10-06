# Using Make: The Basics
#
#
* When running make from a terminal, the make utility will search for a makefile in its working directory. This file is usually just named "makefile" without a sepecific file extension.
    * Some "flavors" of Make use their own filenames  
    (e.g. GNU make may use a GNUmakefie)
* The makefile itself consists of rules that are used to make targets. Each rule has an optional list of dependencies and 