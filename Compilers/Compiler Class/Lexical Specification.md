We can use [[Grammars and Languages | Regular Expressions]] to help us specify.

Example
	writing regex for "if" "else" "then"
		If
			'i''f' + 'e''l''s''e' +...
			"if" + "else" + "then"
	non-empty string of digit
		digit= '0' + '1' +... + '9'
		digit digit*
			Gives you at least one digit, then anywhere from '0'-'9' digits
			ALSO KNOWN AS
				digit+
	letter = 'a'...'z'union 'A'...'Z'
		Tedious, so instead, use this:
			letter = [a-z A-Z]
		letter(letter + digit)*
	Whitespace:
		(''+'\n'+'\t')+


| Type           | New way             | Old Way    |
|----------------|---------------------|------------|
| At Least one   | A+                  | AA*        |
| Union of       | A\|B                | A+B        |
| Option of      | A?                  | A+ Epselon |
| Range          | 'a'...'z'           | [a-z]      |
| Excluded Range | complement of [a-z] | [^a-z]     |


We may know how to deal with large strings, but we don't yet know how to divide up our language into their composite tokens using just our regex.

Write down a whole set of regular expression for each set of our token classes
	Number = digit+
	keyword = 'if' + 'else' +...
	identifiers = letter(letter+digit)*
	OpenPar = '('
	...
From there, construct R, the regex/language of ALL of the lexemes for ALL tokens together

