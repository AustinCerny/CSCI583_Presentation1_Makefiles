# Using Make: Clean and All Targets
#
#
* Another common practice when using Make is to have special targets **all** and **clean**
* Make all is used to make all targets in the makefile. The targets names can be listed without any dependencies
*       all: 
            target1 target2 target3
    * Calling Make all is not the same as calling Make without and additional parameters. Calling just Make will default to building the first target that doesn't begin with a ``.`` character.
* Make clean is used clean up any compiled files out of the directory in case they are bad builds or in order for a directory to be sent elsewhere and compiled on a different system with a different architecture
*       clean:
            rm target1.o target2.o target3.o
* the rm command will remove specific files. The ``*`` expression can be used to match all files of as specific filetype (i.e. *.o will remove all object files
* The all and clean targets are sometime called **PHONY** targets because they do not actually produce a executable called all or clean. It is recommended to specifiy these are phony targets in the makefile as shown
*       .PHONY : clean all
* This will prevent a target called all or clean being created later.