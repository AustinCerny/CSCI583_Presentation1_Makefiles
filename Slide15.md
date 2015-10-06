# Makefile Complaints and Alternatives
#
#
* Make is not necessarily the right utility for all software projects. 
    * Though it is very widely used, it is not as dominate in the industry as it used to be
* For simple programs with few dependencies, creating a makefile can take more time than it saves.
* Large Makefiles can also become problematic.
    * Some projects have 1000+ line makefiles that need to be debugged constantly.
    * Like all pieces of code, makefiles should be commented approprately, comments in a makefile begin with the ``#`` character.
    * In some situations it is advantageous to have multiple makefiles for different parts of a piece of software. Multiple makefiles can be executed at once using
    *       make -f makefile1 makefile2 makefile3 ...