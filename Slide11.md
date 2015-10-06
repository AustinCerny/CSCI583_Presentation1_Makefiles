#  Using Make: Macros (cont.)
#
#
* The example below shows a makefile were macros are used exclusively in 2 targets that share dependencies.
*       CC=gcc
        CFLAGS=-c -Wall
        SOURCES= target1.c target2.c helper1.c helper2.c
        LDFLAGS= -lm -lpopt
        
        Target1: $(SOURCES)
            $(CC) $(LDFLAGS) $(CFLAGS) -o $@
        Target2: $(SOURCES)
            $(CC) $(LDFLAGS) $(CFLAGS) -o $@
* Notice that both Target1 and Target2 use the same macros. This means that if the user wants to change which complier they are using or add a linker to use a new library, they will only have to change 1 line of the makefile. 
* In practice the dependencies of 2 targest are unlikely to be exactly the same, but a program can still compile if it's given a dependency it doesn't use so keeping a single list of all dependencies is feasible. This would cause some unecessary recompilation of certain targets if unused dependencies are updated. 