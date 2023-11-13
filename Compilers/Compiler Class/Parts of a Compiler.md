Step 1: Lexical Analysis
	Reconize keywords
		example: "This is a sentence"
			four keywords(tokens), periods, and separators.
	lexical analysis
		"if x == y then z =1; else z = 2;"
		keyword tokens, separator tokens,


Step 2: Parsing = diagraming expressions
	This   line  is   | a  longer   sentence
	article noun verb | art adj       noun
		subject       |     object
				    Sentence


Step 3: semantic analysis
	For catching inconsistencies
	While we have ambiguities in normal language, programming languges don't allow for such issues.
	variable bindings

Step 4: Optimization
	akin to editing: Making the program run faster and uses less memory
	or reducing power
	or network messages
	database
	example:
		if x and y are int, then x = y* 0 is the same as x = 0
		Else, it doesn't evaluate or evaluates to NaN

Step 5: Code Gen
	Produces assembly code or transpiles into another language

Proportions have changed since FORTRAN
	small lexing, small parsing, large semantic analyisis, HUGE optimization phase, and small code gen phase.

