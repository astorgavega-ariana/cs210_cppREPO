# Dev Log

# (09/11/26)
Per the email we recieved last night on forgetting cloning the bootcamp repo and instead
forking it from github, I decided to get a semi-head start for the assingment -- bringing
everything from the cloned version to my forked one and then wrote some light pseduo code
on how to do what is required for 03_adt_stack. 

After bringing everything to this new project/repo/forked repo, I ran all the programs we
worked on to make sure they executed (and they did!) before realizing I really have no idea how to correlate the 03_adt_stack 
functions to the list of data_ it is connected too. I will use tommorow to do more research on that via youtube but I am
glad I was able to do some pesduo code to at least give me an idea on what the final result should look like and where I need
to bridge the gap in my mind vrs C++ logic.


# (09/12/26)
Continuing off of where I left off yesterday, I started debugging/coding out my psuedo-code on Stack.cpp running into a couple difficulties
over the Stack peek() function and size() function too! I was able to figure them out using a loooot of help from W3 schools (https://www.w3schools.com/cpp/cpp_arrays_size.asp) and
a few reddit rabbit holes to complete before running into a linking problem when trying to execute my code. After getting past that, my code runs perfectly fine but finishes with an exit
code of 139 -- which after a quick google search seems to be a segmentation fault error of sort? So I will try to get past that and into exit code 0 next time.

# (09/13/26)
I resolved the segmentation fault error by adding an initializer to my stack.cpp after learning that c++ doesn't really assign a default value to objects, which had temporairly
fixed my execution exit code back to 0 but didn't allow the bigger problem ahead I hadn't realized after a lengthy run of all the files inside 03_adt where (at a very late time in the night and early morning) 
many of my functions simply weren't running because they lacked any real "logic" and action, following useless loops I accidently created without realizing. Having to go through a whole thing with all my files and re-doing
my initial code, I finally got my code running and logic making much more sense with all print statements accurate to the push,pop,peek,etc functions I was using on the data stack list.

# (09/14/26)
Final day of the assingment and pretty much done with the reflection questions back on my code, I have taken a lot into consideration about my code following these questions
especially on what I would do differently. For example, on reflection questions 4 and 5 where I was asked about trying to implement fucntions like push() or pop() when the stack is full or empty which I hadn't really taken into
account when doing my code. I could definitly see how helpful those like "edge" cases could be, especially in a fully fledged program so if I had more time and more thought into my code I'd defintly add that. In terms of explaining why I didn't
have that I'd say it was because 1. I didn't really think about edge cases while coding because I was just trying to get the actual code/program to execute correctly first and 2. Although it would be very good coding practice to just have and test for, it slipped off
my mental checklist because it wasn't necessarily listed on the assingment requirements. Nonetheless, I recgonize what I could've done to make my code even better.
