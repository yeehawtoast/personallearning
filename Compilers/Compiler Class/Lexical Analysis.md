 
What we see:
```
if (i==j)
	z = 0;
else
	z = 1;
```

What the machines sees:

`\tif (i==j)\n\t\tz=0;\n\telse\n\t\tz=1;`

Needs to classify the strings according to their role
	in english
		noun, verb, adverb, adjective
	in programming
		identifier, keywords, (), ;, numbers, '',etc.

Identifiers- Strings of letters or digits, starting with a letter.
Ints - a non-empty string of digits
Whitespace- a non-empty sequence of blanks, newlines, tabs


Classify program substrings according to role
Communicate Tokens to the parser

White Space
Keywords
Variables
Numbers
Single Char token classes
assignments
operators


Lexical analysis needs to identify the lexemes
and identify the token class of each lexeme


Problems in LA:
	1. Lookahead
		1. We need to see what is going on when and where
		2.  = || ==
	2. Maximal Munch

These problems are solved by [[Lexical Specification]]


For understanding languages themselves, we need to look at [[Grammars and Languages]]

When we have defined our Lexical Specifications, we can go back to analysis and define our ruleset for breaking down our whole buffer into their composite lexemes.
	Let input be x1...xn
	for 1<=i< n check
		x1...xi E L(R)
	(*Checking our inputs to make sure they are in the language of R*)
	If success, then we know that xn is in our language. Remove xn from input and go back


# Questions
How much input is used?
	let us assume
		x1...xi < x1...xj && i!=j
		which of these tokens do we use?
		example:
		= vs ==
	ANSWER: 
		**Maximal Munch**: Always take the longer of the inputs
Which token is used?
	For example: Technically, if is in the language of both keywords and identifiers. Which one wins?
	**Priority Ordering**: List the languages by importance and if a lexeme can fit into more than one, pick the higher priority order one.
What if no rule matches?
	**Error strings**: All the strings not in the lexical specification, put it last in priority, which allows the compiler to throw an error
