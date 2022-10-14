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

