# Formal Languages
A formal language has an **alphabet** (or set of characters) denoted by Σ, which the language is a set of strings of characters drawn from Σ.
	Example
		Alphabet = English characters
		Language = English sentences
		*technically not a formal language*
	Example 2
		Alphabet = ASCII
		Language = all valid c programs
Meaning functions
	usually denoted by L
	maps syntax (how a word is spelt) to semantics (what a word means and where it fits in the grammar)
	l(e) = M
	regex maped to a set of strings

example
	epsilon = {""}
	c = {"c"}
	A + B = A union B
	AB = {ab | a in A with b in B}
	A* = Union of i>=0 of A^i
*A and B are alphabets being unioned together*

L maps from expressions into set of strings


Syntax and Semantics are separated from each other because that means we can have two different notations mean the same thing. 

for L, the rule is "many to one" from syntax to semantics. It is why optimization matters. 

NEVER one to many. That's how you get english and other spoken languages.
# Regular Languages
Regular Expressions
		single character
			'c' or {"c"}
		Epsilon
			= {""}
		Union
			A + B = {a|∈A}∪{b|∈B}
		Concatenation
			AB = {ab|a∈A ∧ b∈B}
		Iteration
			A* = the Union for i>=0 of A^i
				One possibility is A^0 = ε
		The regular expressions over alphabet Σ are the smallest set of expression including:
			R = epsilon
				"c"
				R + R
				RR
				R^x
			The set of regular expresions over a given alphabet
	Examples:
		Σ = {0,1}
			1* = "" + 1 + 11 + 111 + 1111 +...
			(1+0)1 = {11, 10}
			0* + 1*
			(0+1)* = "", 0+1, (0+1)(0+1),...
						All strings of 0s and 1s
						Known as Σ*
	Regular expressions are used to define a regular language
		There are five constructs that you can use to build a regular language which denote a set of strings

