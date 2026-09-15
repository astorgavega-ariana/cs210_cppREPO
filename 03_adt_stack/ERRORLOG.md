# Error Log

# (09/11/26)
After playing around with my pesudo code trying to figure out how to 
debug it a bit/make it work, I find that the program won't run even after
adding the functions from the header page (Stack.h) like  void push(int value), 
void pop(), etc. I can tell there needs to be some correlation between data_ and the functions
otherwise how will the program know what it is pushing into the list or out of. 4 error messages linked 
reading:

/Users/ariana.av/CLionProjects/CS210CPPRepo.git/03_adt_stack/Stack.cpp:29:16: error: expected '(' for function-style cast or type construction
29 |  return int top() const;

So I will fix that!


# (09/12/26)
I started debugging and coding about to make the program work per the assingment's instructions before running into a couple errors, mostly logic at first
like my if-else statements and how to properly use the functions from Stack.h like the push and pop functions. After writing all the functions and trying to 
run the actual code, I kept running into this error:

' Undefined symbols for architecture arm64:
"Stack::Stack()", referenced from:
_main in main.cpp.o
ld: symbol(s) not found for architecture arm64
clang++: error: linker command failed with exit code 1 (use -v to see invocation)
make[3]: *** [03_adt_stack] Error 1
make[2]: *** [CMakeFiles/03_adt_stack.dir/all] Error 2
make[1]: *** [CMakeFiles/03_adt_stack.dir/rule] Error 2
make: *** [03_adt_stack] Error 2
'

Initially, I thought it was a logic problem or syntax somewhere in the code, but after looking through all the files and
inserting the error into google and realizing through reddit and stack overflow that it seemed to be some sort of linking problem
which led me back to the CLIST file playing around with that for a bit before a fellow reddit post led me to the realization 
that I needed an initilizer of sorts for my Stack.cpp. With inserting Stack::Stack() my code finally worked! At least to an extent
my code executing but with an exit code of 139. Will resume tommorow.

# (09/13/26)
After re-running and attempting to debug, I finally came to the hint that was in my code all along in the header of the data size being 100 and under it being the variable of topIndex. I hadn't noticed
it at the time and completely forgot about it when adding it after reading the assignment instructions. I suppose the reflection questions I added in 2README 
were also another hint but nonetheless, after realizing I needed a topIndex variable to implement throughout my code I reworked on debugging nearly all my functions to include
some use/manipulation of topIndex. Suprise, suprise, my code finally executed fully with all print statements and an exit code of 0! 

