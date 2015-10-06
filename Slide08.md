# Using Make: Rules
#
#
* Rules begin with a target name followed by a colon and a list of dependents. Then, there is a line break followed by a tab followed by a compile command. 
* The example below shows the rule for a target called hello. 
* 
        hello: hello.c main.c helper.c
            gcc -Wall -lm -o Hello
* This target uses 3 C files, hello, main and helper. It creates the Hello executable and uses the gcc compiler with the ``-Wall`` flag. Includes a math library by using the ``-lm`` flag
* From the command line. typing `` make hello`` will generate the hello.o file based on this rule.
* If the user wants, a target can have more than 1 set of commands associated with it. This can be done by adding a new line begining with a  tab after the compile command. This is not very common however.
