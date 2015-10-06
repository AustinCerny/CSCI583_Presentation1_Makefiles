# Using Make: Important Considerations
#
#
* Make decides if a file has been by checking the last time it was modified. This is not a foolproof solution. If a file is replaced with an older version it will not be recognized as new or changed. It also means a computer that uses make needs an working system clock
* A makefile is not executed line by line like a piece of imperative code in a language like C. The actual order in which steps are executed cannot be specified. In practice this doesn't require any special adjustments but it's worth remembering.
* Line breaks and tabs are not whitespace in a makefile, keep carefull track of where they are used


