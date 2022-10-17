# A-Bugs-Life
# JavaScript's Regex

This is a look in depth to Regex library that comes with JavaScript

## Summary

regular expression, a regex is a string of text that lets you create patterns that help match, locate, and manage text. Users are able to find, replace, and remove the queried pattern from any targeted text. furthermore, we will be taking a look at the regex library that is used with JavaScript. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)


## Regex Components

This regex contains two methods, exec() and test(). These methods are often used in combination with the string methods that are in JavaScript. 


### Anchors

Regex Anchors are used to notate positions, rather than characters. There are to anchor characters in JavaScript's Regex function. 

- ^ - By default, the match must occur at the beginning of the string.
- $ - 	By default, the match must occur at the end of the string or before \n at the end of the string.


### Quantifiers

Quantifiers determine the number of instances a string must have for the searched pattern. 

 +  quantifier matches the preceding element one or more times.
 *  quantifier matches the preceding element zero or more times. It's equivalent to the {0,} quantifier.
 +  Match one or more of the previous
 \	Used to escape a special character
 ?  quantifier matches the preceding element zero or one time. It's equivalent to {0,1}
 $	End of a string.
 ^	Beginning of a string. Or within a character range [] negation.
 ?=  matches any string that is followed by whatever character is placed after the =. 
 ?!  matches any string htat is NOT followed by whatever character is placed after the =. 
 {X}  specifies the number of characters that must be in a row. 
 {X,}  matches any squence of X numbers. 
 {X, Y}  matches a sequence of numbers from x to y.
 {\b }  Start at a word boundary.
[A-Z]	Matches an uppercase character from A to Z.
(\w*?\s*?) - Matches zero or more word characters, followed by one or more white-space characters but as few times as possible. This pattern is the first capturing group.
{1,10}  Matches the previous pattern between 1 and 10 times.
[.!?]  Matches any one of the punctuation characters ., !, or ?.


### OR Operator

A "|" is used to as an OR operator in the JavaScript regex. If multiple patterns are being searched, can be seperated with the |


### Character Classes

Character classes identifies the type of character or characters being searched for.

 [abcd] or [a-d]  both patterns do the same thing. The first matches each of the characters listed  while the second matches any characters within specific range
 ^  Using this NOT operator in front of the patterns means it matches any strings that do NOT contain the specified characters (or characters within the range).
 .  Can match the literal . or can denote that a character must have something either before or after it. 
 d  Matches any numeric value. 
 D  Acts as the NOT operator for d. 
 w  Matches any character (excluding special characters).
 W  Acts as the NOT operator for w.
 s  Matches spacing.
 S -Acts as the NOT operator for s.


 ### Flags

 Flags are to specify  allowed parameters within a search. 
s  - allows a dot to act as a newline character.
i - specifies case does not matter for the characters used in the pattern.
m  - traverses multiple lines of a queried string.
y  - searches the exact position of the pattern.
g  - returns all instances of the pattern, instead of just the first.
u  - allows Unicode support.

 
 ### Grouping and Capturing

 In Javascript's regex,() means either of the patters can appear in the queried text.Then  [] targets groups of characters that are being searched for, as mentioned above. 
 

 ### Bracket Expressions

 Bracket expressions simply reference the form-factor of the grouping characters. 
 

 ### Greedy and Lazy Match

 Greedy and lazy is what is returned from a matching pattern. ? will stop after the first instance while * is considered greedy, because it will continue for each sequential matching character.
 

 ### Boundaries

 The boundary operator \b  searches word positioning.
 

 ### Back-references

 Back-references is used to store found value and group items found in between those symbols/named instances. 
 

 ### Look-ahead and Look-behind

 There is a combination of four types of "lookaround" operators:
 - X(?=Y) - This pattern is called a positive lookahead, and would match any instance of X that is followed by Y.
 - X(?!Y) - Is the negation of the previous example. Known as a negative lookahead.
 - (?<=Y)X - This pattern is called a positive lookbehind, and would match any instance of X that is behind Y. 
 - (?<!Y)X - Is the negation of the previous example. Known as a negative lookbehind. 
 

 ## Author

 [Joel A Rivera Rivera](https://github.com/Jrivera239)
 
 I have commited myself to become a fullstack developer. I have choosen different careers in my life but never been as determine as I have with developer. I currenty reside in Kissimmee, Florida and am absolutely willing to relocate for a greater future in life. I'm a dedicated individual who pursuits goals and this is a goal of mine with many more to accomplish.