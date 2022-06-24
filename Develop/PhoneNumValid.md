# Regex (Phone number validation)

A regular expression is a group of characters or symbols which is used to find a specific pattern in a text.

A regular expression is a pattern that is matched against a subject string from left to right. Regular expressions are used to replace text within a string, validate forms, extract a substring from a string based on a pattern match, and so much more. The term "regular expression" is a mouthful, so you will usually find the term abbreviated to "regex" or "regexp".

Imagine you are writing an application and you want to set the rules for when a user chooses their phone number. We want to allow the username to contain numbers, underscores and hyphens. We also want to limit the number of characters in the username so it does not look ugly. 

i.e For this tutorial the type of regEx I chose to validate is phone number. 


## Summary

We can use the following regular expression to validate the phone number:

 /\(?([0-9]{3})\)?([ .-]?)([0-9]{3})\2([0-9]{4})/



To get a better understanding of what it entails, here is a breakdown of all the elements.

/^\(?: One of the optional forms of the number may start with an open parenthesis.


([0-9]{3}):  Start of the pattern can be  any number between  0 and 9 which is  of length 0  or or 9.

The curly brace - means repeat the first pattern[0-9] three times. 

\)?: This provides an option to include a close parenthesis.
[- ]?: The string may optionally contain a hyphen either after the parenthesis or following the first three digits.
([0-9]{3}): This means any number between  0 and 9 which is  of length 0  or or 9.

(\d{3}): Then the number must contain another three digits. Depending on your previous options, it can look like (214)-753, 541-753.

[- ]?: Once again, you can include an optional hyphen in the end – (214)-753-, 541-753-.
(\d{4})$/: Lastly, the sequence must end with a four-digit sequence. It can look something like (214)-753-6010, 214-753-6010, 214753-6010, or 214753-6010

 

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
^:	Caret is an Assertion (Anchor)	that Matches the beginning of a line.
$	The Dollar Sign	is an Assertion (Anchor) that	Matches the end of a line.
\b	Word Boundary is an Assertion (Anchor) that	Matches a word boundary (a non-word character such as a space, tab, or period).

### Quantifiers
Quantifiers allow for some flexibility in matching as they define the number of times a character, pattern, or group appears in a regex match.

{ }	Curly Braces is a Quantifier RedEx type and we can use it to Creates a specific numerical quantifier range.
(?)	Question Mark is Quantifier	RedEx type that Matches zero or one preceding character.
(+)	Plus Sign is a Quantifier RedEx type that Matches one or more preceding characters.
(*)	Asterisk is a Quantifier RedEx type that	Matches zero or more preceding characters

### Grouping Constructs
[ ]	Square Brackets and ( )	Parentheses	Grouping RedEx type	


### Bracket Expressions
( )	Parentheses	is a Grouping RedEx type and it used to Creates a sequence or sub-expression.
[ ]	Square Brackets	is a Grouping RedEx type and it used to Creates a character group or range.
{ }	Curly Braces is a Quantifier Redex type and it used to Creates a specific numerical quantifier range.
### Character Classes

### The OR Operator
Vertical bar | is used for alternation (or operator).


### Flags
i: This flag means that it is case insensitive, which means that the entire expression is not case sensitive.
g: This flag means a global search that maintains the index of the last match so that subsequent searches can start at the end of the previous match. Without the global flag, subsequent searches will return the same match.
m: This flag means multi-line. When the multi-line flag is on, the start and end anchors (^ and $) match the beginning and end of a line, not the beginning and end of the entire chain.
u: This flag means Unicode. Users can use extended Unicode escapes of the form \ x {FFFFF} by activating this flag.
y: This flag means sticky. The expression only matches its lastIndex position and ignores the global flag (g) if it is set. Since every search in RegEx is discrete, this indicator has no further effect on the displayed results.
s: This flag means dotAll. A period (.) matches each character, including the new line.


### Character Escapes
\	Backslash or Escape Character 
BRE: Indicates the proceeding character is special.
ERE: Indicates the proceeding character is basic.

## Author

 For inquiries related to repo and additional questions

Reach out to me on Github: [DemeSibere](https://github.com/DemeSibere)<br />

Email me: demesibere16@gmail.com

----