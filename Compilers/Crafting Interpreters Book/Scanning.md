 Other names: Lexing, Lexical Analysis

# What is Scanning?

I write down character onto a screen and they have meaning to my brain. How? To start, my brain needs to put certain characters together into something called lexemes or tokens
### Lexeme
A basic [lexical](https://www.google.com/search?client=firefox-b-1-d&sca_esv=577907868&sxsrf=AM9HkKmNOr6X5eWIsMCxPb-L53RCECDK5A:1698695877836&q=lexical&si=ALGXSla6aFUzqw8hZDovT8H5OBVEPRVVxh1CE_cNRL0Nj5jnEuV4qs6-fKekJdd3K2tIXYbL_v6TZkGGk0-5ItuhROkeLa-G0jiKMqihPqWZ_QloBy_hMvE%3D&expnd=1) unit of a language, consisting of one word or several words, considered as an abstract unit, and applied to a family of words related by form or meaning.


For the code above, we can break our lexemes into *var*, *lanugage*, *=*, *"lox"*, and *;*

While some of these these words don't have inherent meaning (like `"lox"`) some of these lexemes can have specific meanings. These **keywords** are also known as **tokens**. 


### Example:
I can understand "The Dog Ran Fast" or "El Perro Corre rapidemente" as both of these languages

# Exercises
1. The lexical grammars of Python and Haskell are not _regular_. What does that mean, and why aren’t they?
    
2. Aside from separating tokens—distinguishing `print foo` from `printfoo`—spaces aren’t used for much in most languages. However, in a couple of dark corners, a space _does_ affect how code is parsed in CoffeeScript, Ruby, and the C preprocessor. Where and what effect does it have in each of those languages?
    
3. Our scanner here, like most, discards comments and whitespace since those aren’t needed by the parser. Why might you want to write a scanner that does _not_ discard those? What would it be useful for?
    
4. Add support to Lox’s scanner for C-style `/* ... */` block comments. Make sure to handle newlines in them. Consider allowing them to nest. Is adding support for nesting more work than you expected? Why?