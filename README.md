# Matching an Email: A Regex-Tutorial By Rob Lemus

Introductory paragraph (replace this with your text)

## Summary

Generally, a regular expression is a sequence of characters that defines a search pattern for text. In other words, given a specific pattern, you can take the literal characters or even meta characters from that pattern to search through a body of text. Literal characters being more specific and strict versus meta characters having a more generalized definition on the pattern.

An email regular expression will allow the user to validate the exmail address being provided. This type of redex is typically utilized to reduce the number of emails returned as undeliverable. With email, validation can be tricky as there is no unversal rule or deifnition for what constitutes a valid email or not. For example, your regex may accept test@test.com as a valid email, however, you would not know if it is truly valid unless you sent an email to it and tried it yourself. Below you will find a sippent of an email regex:

^[\w!#$%&'*+/=?`{|}~^-]+(?:\.[\w!#$%&'*+/=?`{|}~^-]+)*@↵
(?:[A-Z0-9-]+\.)+[A-Z]{2,6}$


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)


## Regex Components

### Anchors
Anchors are regex components that allow for the search to determine what type of regex it is searching for. For email regex you can use the ^ symbol to define the start of a string, and the $ to define the end of a string. 

### Quantifiers
Quantifiers set the character count for the search within the string. Specifically for email, the symbols + and * are used. The + symbol will take the preceding string of character count and repeat the search 1 or more times, whereas the * symbol repeats the search 0 or more times.

### Grouping Constructs
Grouping constructs allow for the search to be more defined and find a string of characters. 

### Bracket Expressions
Bracket expressions are considered character classes. It essentially gives a range of characters allowed within a search. Oftentimes the classes can be specific or more general. Within email, this expression [A-Z0-9.-] allows letters between A and Z, numbers between 0 and 9, and symbols . and -

#### Character Classes
- Literal Characters
Literal characters are specific and need to follow a specific order and meet exact criteria to match with the sequence when used for search. For example, a search for the word RAINBOW could be defined by restricting only those specific characters to be searched for (Capital R, and all subsequent lower case letters after it).

- Meta Characters
Meta characters have a more generalized approach in their search of the pattern. For example, a search of the word RAINBOW through meta characters could be defined by allowing for any vowel to come after the first R.

- Email Specific
Specific to email we have the <\S> character class which mataches characters that are not whitespace. This is very important for email verification.

### The OR Operator
This operator allows for grouping and alternation between characters to find patterns defined.

### Flags
Generally speaking, flags allow for additional function or restrictions. The flags include g for global search, i for case-insensitive search, and m for multi-line search.

### Character Escapes
Character escapes are utilized as tools to ensure there is no misinterpretation of a defined search. For example, in an email search, an @ and . symbol could be misinterpreted as literal symbols. In order to avoid this, you could use character escape: \

## Author

Rob Lemus is a student at the UM Coding bootcamp program. He currently works for a large media company and hopes to take this new skill and build onto his career with it.
https://github.com/rnl0396
