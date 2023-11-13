As far as programming is concerned, “arithmetic” is half the game; the other half is “algebra.” Of course, “algebra” relates to the school notion of algebra as little/much as the notion of “arithmetic” from the preceding chapter relates to arithmetic taught in grade-school arithmetic. Specifically, the algebra notions needed are variable, function definition, function application, and function composition. This chapter reacquaints you with these notions in a fun and accessible manner.


A program rarely consists of a single function definition. Typically, programs consist of a main definition and several other functions and turn the result of one function application into the input for another. In analogy to algebra, we call this way of defining functions composition, and we call these additional functions auxiliary functions or helper functions. 


Consider the program of figure 12 for filling in letter templates. It consists of four functions. The first one is the main function, which produces a complete letter from the first and last name of the addressee plus a signature. The main function refers to three auxiliary functions to produce the three pieces of the letter—the opening, body, and signature—and composes the results in the correct order with string-append.


From a coding perspective, a program is just a bunch of function and constant definitions. Usually one function is singled out as the “main” function, and this main function tends to compose others. From the perspective of launching a program, however, there are two distinct kinds:

- a batch program consumes all of its inputs at once and computes its result. Its main function is the composition of auxiliary functions, which may refer to additional auxiliary functions, and so on. When we launch a batch program, the operating system calls the main function on its inputs and waits for the program’s output.
    
- an interactive program consumes some of its inputs, computes, produces some output, consumes more input, and so on. When an input shows up, we speak of an event, and we create interactive programs as event-driven programs. The main function of such an event-driven program uses an expression to describe which functions to call for which kinds of events. These functions are called event handlers.
    
    When we launch an interactive program, the main function informs the operating system of this description. As soon as input events happen, the operating system calls the matching event handler. Similarly, the operating system knows from the description when and how to present the results of these function calls as output.
    

This book focuses mostly on programs that interact via graphical user interfaces (GUI); there are other kinds of interactive programs, and you will get to know those as you continue to study computer science.

Batch Programs As mentioned, a batch program consumes all of its inputs at once and computes the result from these inputs. Its main function expects some arguments, hands them to auxiliary functions, receives results from those, and composes these results into its own final answer.

Once programs are created, we want to use them. In DrRacket, we launch batch programs in the interactions area so that we can watch the program at work.

Programs are even more useful if they can retrieve the input from some file and deliver the output to some other file. Indeed, the name “batch program” dates to the early days of computing when a program read a file (or several files) from a batch of punch cards and placed the result in some other file(s), also a batch of cards. Conceptually, a batch program reads the input file(s) at once and also produces the result file(s) all at once.
# Exercises
Exercise 11. Define a function that consumes two numbers, x and y, and that computes the distance of point (x,y) to the origin.

In [exercise 1](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._arith-n%29%29) you developed the right-hand side of this function for concrete values of x and y. Now add a header.[](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._fun0%29%29)

Exercise 12. Define the function cvolume, which accepts the length of a side of an equilateral cube and computes its volume. If you have time, consider defining csurface, too.

Hint An equilateral cube is a three-dimensional container bounded by six squares. You can determine the surface of a cube if you know that the square’s area is its length multiplied by itself. Its volume is the length multiplied with the area of one of its squares. (Why?)[](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._fun1%29%29)

Exercise 13. Define the function string-first, which extracts the first [1String](https://htdp.org/2023-8-14/Book/part_one.html#%28tech._1string%29) from a non-empty string.[](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._fun2%29%29)

Exercise 14. Define the function string-last, which extracts the last [1String](https://htdp.org/2023-8-14/Book/part_one.html#%28tech._1string%29) from a non-empty string.[](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._fun3%29%29)

Exercise 15. Define ==>. The function consumes two Boolean values, call them sunny and friday. Its answer is #true if sunny is false or friday is true. Note Logicians call this Boolean operation implication, and they use the notation sunny => friday for this purpose.[](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._fun4%29%29)

Exercise 16. Define the function image-area, which counts the number of pixels in a given image. See [exercise 6](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._arith-i1%29%29) for ideas.[](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._fun5%29%29)

Exercise 17. Define the function image-classify, which consumes an image and conditionally produces "tall" if the image is taller than wide, "wide" if it is wider than tall, or "square" if its width and height are the same. See [exercise 8](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._arith-b2%29%29) for ideas.[](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._fun10%29%29)

Exercise 18. Define the function string-join, which consumes two strings and appends them with "_" in between. See [exercise 2](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._arith-s0%29%29) for ideas.[](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._fun10a%29%29)

Exercise 19. Define the function string-insert, which consumes a string str plus a number i and inserts "_" at the ith position of str. Assume i is a number between 0 and the length of the given string (inclusive). See [exercise 3](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._arith-s1%29%29) for ideas. Ponder how string-insert copes with "".[](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._fun10b%29%29)

Exercise 20. Define the function string-delete, which consumes a string plus a number i and deletes the ith position from str. Assume i is a number between 0 (inclusive) and the length of the given string (exclusive). See [exercise 4](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._arith-s2%29%29) for ideas. Can string-delete deal with empty strings?[](https://htdp.org/2023-8-14/Book/part_one.html#%28counter._%28exercise._fun10c%29%29)