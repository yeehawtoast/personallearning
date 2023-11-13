## The Key Idea:
1. Computing is about **data**, period, end of story. That is all it is about. How we move our data, how our data can layer ontop of itself to produce greater complexity, how our data is used or how our data interacts with the general public (movies, video games, television, etc.) Regardless, at the end of the day, all it is is data. 
2. If all we do is data, then we can use mathematics on that data, even if it is complex or describing concepts like motion (linear algebra), or is used to express how to make things better (optimization).

    (define (y x) (* x x))
    This is just like:
``` javascript
    function y(x){
	    x= x*x
    }

```

the formula in racket is: 

> ([define](http://docs.racket-lang.org/htdp-langs/beginner.html#%28form._%28%28lib._lang%2Fhtdp-beginner..rkt%29._define%29%29) (FunctionName InputName) BodyExpression)

and when running the function:

> (FunctionName ArgumentExpression)

This is how LISP works and Racket is based on LISP.


Early Programming Languages were based purely on math and take their ideas from math:

1. Functions
	1. y = mx+b
	2. You can think of y as being a function name
	3. the function "y" has 3 variables: "m" "x" "b"
	4. We multiply m and x and then add b to the result

2. sign (signum)
	1. Signums are just conditionals in programming or switch cases

>Good programming is far more than the mechanics of acquiring a language. Most importantly, it is about keeping in mind that programmers create programs for other people to read them in the future. A good program reflects the problem statements and its important concepts. It comes with a concise self-description.

>In short, good programming is about solving problems systematically and conveying the system within the code. Best of all, this approach to programming actually makes programming accessible to everyone—so it serves two masters at once.

