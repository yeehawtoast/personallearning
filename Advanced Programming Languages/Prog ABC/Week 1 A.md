- An ML Program is a sequence of *bindings*
- Our bindings are *type-checked* and then *evaluated*

### variable bindings

val x =e;

val is a *keyword* and e is any *expression* 

## Rules for Expressions
```sml
val x =34;
val y = 17;
val z = 70;
val q =71;

```

you can have expressions within expressions
Every expression has:
	**syntax
	type-checking rules**
		produces a type or fails
	**evaluation rules**
		produces a value or exception or infinite loop

Variables
	syntax
	type checking rules
		ML: Look in static environment
	Evaluation:
		Look up value in the current dynamic environment

Additon
	e1 + e2  unless the types differ, then throw error


conditionals
	if e1 (always bool) then e2 else e3

## The Repl and errors
read eval print loop
	read what we have inputed
	evaluate it
	print the results of that evaluation
	loop back so that we are back to the input

## Shadowing
you cannot change or mutate a variable after it has been created, but you can redefine it at a later point. 

Example:
```sml
val a = 1
val b = a
val a = 2
```
In this instance, we can see a static environment where a is bound to 1. B is then bound to whatever a's value is in the static environment at that moment. a new variable a is bound to 2, but b does not change, instead we create a new dynamic environment where a is bound to 2.

This is because you are not "assigning" a to 1 or 2. Assignment does not happen in ML. Rather you evaluate the expression and whatever the variable is bound to. 

in ML this is an **eager evaluation** while Haskell family languages use ***lazy evaluation*

## Functions
building blocks of any language. 

fun(para : type, para : type) =


you can use previous bindings in further functions and a function can call itself. cannot refer to future function bindings. 

We will discuss recursion later, but its a lot better.

A function is a value which adds x0 to the environment and doesn't return a type yet so that later expressions can call it.

the return type of x0 will be whatever is evaluated by the function.

When a function is defined does not mean that the function is being use or "called". nothing can be evaluated until the function is called.

To evaluate a called function:
	evaluate e0 to a function fun x0(x1:t1,..., xn:tn) = e
	evaluate arguments to values v1, ...,vn
	result is evaluation of e in an environment.

## Pairs and Tuples
	(e1, e2)
	eval e1 to v1 and e2 to v2
	if e1 has type ta and e2 has type tb, then the type of the tuple is ta * tb

acessing pairs
	#1 e and #2 e
You can nest pairs and tuples
# New Words
Binding
Type-checking
evaluation
static and dynamic environment
context
syntax
Eager Evaluation
	Eager evaluation is when an evaluation is executed as soon as it is encountered. This means that the compiler will bind an evaluation before the code is finished. This is the "old school" way of evaluating
Lazy Evaluation
	Evaluation happens when the 