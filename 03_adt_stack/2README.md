# Reflection Questions
1. What value does topIndex hold immediately after construction, and why does that specific value make isEmpty() return the right answer with no special-casing?
- Immediately after construction I imagine it's default value is 0 because thats what any default value of an array would be but in actuality it has a default value of -1 because a default value of 0
doesn't allow isEmpty() to return the right answer but when it has a default value of -1 the value is just reporting back an empty stack list aka void but at 0 the list should have at least 1 item in it which makes sense
because 0 is the first position in an array so it makes sense to assume there is a value at 0 and none at -1.

2. Walk through push step by step, in words: what happens to data and topIndex, in what order, and why would swapping that order break the stack?
- For the push() function to work, I have topIndex increment itself to iterate through the array list and then assign topIndex from the stack list (so keeping track of its placement in the stack) to its current value of the stack list.
If this were swapped, it would be automatically be problamatic because the first value topIndex would be assinged to would be -1 and -1 is TECHNICALLY out of bounds since it is not 0 (the first place in the stack) nor any real value.
3. Give the time complexity of push, pop, peek, isEmpty, isFull, and size, individually, in Big-O. For each one, justify it by describing what your code actually does, not by naming the general rule for stacks.
- I'm pretty sure the time complexity of all these functions have a constant time complexity aka O(1) (a little skeptical of peek because of its if-else) but for the most part, none of these functions are utlizing any loops or multitude
iterations of "n" to make it more than O(1).
- In push() has a time complexity of O(1) because it is simply incrementing and reassigning value which takes constant time no matter the fixed stack array value. For pop(), also O(1), it is just subtracting so also a constant function. 
peek() is simply accessing data it is accessing a single element at value in array so its index and returns it so constant. isEmpty() is a boolean fucntion which evaluates once (false or true) making it constant with topIndex == -1. isFull() same thing as isEmpty but with topIndex being 99 for this array.
size() just takes topIndex and adds 1 (with casting) making it a one single operation aka constant O(1).
4. Exactly what happens in your code when push is called while the stack is full? State what prints (if anything), what gets returned (if anything), and whether topIndex changes. Then say why you chose that behavior.
- I didn't add any real "edge" cases -- like what would happen if push is called to a full stack or what gets returned but I imagine if I were to impelement it would be an if-else statement with a message sayign the function
is not possible because the stack is full likely to just return that message and maybe a void value since its an "illegal" arg? In this scenario, topIndex wouldn't change either since it wouldn't increment and stay at the last place in the stack with would be 99!
5. Exactly what happens when pop or peek is called while the stack is empty? Same level of detail as above.
Again, I don't have any cases for a message or interception to occur if pop and peek were called while the stack is empty but if I DID, then again, a message saying the stack is empty and therefore cannot peform these actions, return a void value, and topIndex continue where it starts origionally
since it won't increment.
6. Your array is fixed at 100 slots. If a caller needed more room than that, what would have to change in your class to support it, and what would it likely cost in terms of the time complexity you gave in question 3?
- In java I remember doing a whole thing where I would copy the array I was trying to increase only to transfer it to a new array where it would extend the original array's size by double as needed. In terms of this scenario, I'm not exactly sure off the top of my head on how to go about in especially in c++ but I know
I would need to likely do something along the lines of copying and resizing the array since an array is usually the fixed number of slots aka 100 here. In terms of time complexity, I don't think I'd need any nested loops of any sort to do the resizing so I will go ahead a lump it with the O(1) the rest of my functions use maybe using O(N)
as a worst worst case?
7. Without looking anything up: if this stack were built on a linked list instead of an array, name one advantage and one disadvantage that trade-off would bring, based on what you already know about how arrays and pointers behave differently.
- If the stack were a linked list, I think a good advantage would be the size constraint like an array usually has a fixed size or needs an extra function to keep increasing the fixed size but a linked list I think I remember can grow/shrink because of its pointers?? For sure I know a BIG
disadvantage is the differences in accessing data -- arrays waaaaay better for accessing a very specfifc element while linked lists usually have to go through the entire thing to find.