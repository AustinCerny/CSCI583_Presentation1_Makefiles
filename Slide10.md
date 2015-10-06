# Using Make: Macros (cont.)
#
#
* There many common conventions for using macros including this list of variables names pertaining to C and Cpp codes
* 
        Macro   Description                     Example    
        CC      Compiler for C programs         cc
        CXX     Compiler for C++ programs       gcc
        CFLAGS  Flags to give to the compiler   -g -Wall
        LDFLAGS Linker Flags                    -lm
* There are also special macros for predefined for make including (but not limited to).
*       $@ refers to the name of the target
        $< refers to the name of the first dependency
        $? refers to the names of all dependencies that are newer than the target
        $^ refers to all dependencies of the target with duplicates removed
        
