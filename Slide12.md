# Using Make: Advanced Macros
#
#
* Macros can be edited and new macros can be created using certian commands
    * Parts of a macro can be substited using the ``=`` operator
    *       CPPFILES = file1.cpp file2.cpp file3.cpp
            OFILES = $(CPPFILES:.cpp=.o)
            # OFILES is file1.o file2.o file3.o
    * Elements of 1 macro can also be subtracted from another
    *       LIST0 = file1 file2 file3 file4
            LIST1 = file1 file2
            LIST2 = $(LIST0)-$(LIST1)
            # LIST2 is file3 file4
* Macros can also be substituted from the command line  
 Calling ``make CFLAGS="-Wall -g" target1`` will make target1 executable while overwritting the CFLAGS macro in the existing makefile.