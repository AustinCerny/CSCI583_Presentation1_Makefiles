# Using Make: Macros
#
#
* An important feature of make is its ability to use macros. Macros are analogous to variables in programs. A macro is defined using the ``=`` character  
*
        MACRO = -mymacro
*  In order to use a macro, we need to use a dereference operator ``$``
*  
        $(MACRO)
* Macros can also be lists, which can simplify the rules of a makefile considerably. The example below shows how the previous hello rule can be simplified with a macro
* 
        DEPENDS = hello.c main.c helper.c
        hello: $(DEPENDS)
            gcc -Wall -lm -o Hello
* If multiple targets have the same dependencies, using macros will make a makefile more concise and easy to understand. Macros are often used in all parts of a rule

