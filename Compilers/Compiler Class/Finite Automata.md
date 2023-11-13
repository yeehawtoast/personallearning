Difference between regex and finAu

Regex = Specification
Finite Automata = implementation


- Input alphabet
- finite set of states
- start state
- set of accepting state
- set of transitions

## transitions
example: 
	In state 1 and you receive input a, then transition to state 2
	"In state S<sub>1</sub> on input *a* go to state S<sub>2</sub>"
	If end of input and in accepting state => accept
	Otherwise => reject
		terminate in state not a final state
		gets stuck
