# A-Bugs-Life
# JavaScript's Regex
Regular expressions are patterns used to match character combinations in strings. In JavaScript, regular expressions are also objects. These patterns are used with the exec() and test() methods of RegExp, and with the match(), matchAll(), replace(), replaceAll(), search(), and split() methods of String. This chapter describes JavaScript expressions.

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

- ^The        matches any string that starts with The
- end$        matches a string that ends with end
- ^The end$   exact string match (starts and ends with The end)
- roar        matches any string that has the text roar in it


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
- abc*        matches a string that has ab followed by zero or more c
- abc+        matches a string that has ab followed by one or more c
- abc?        matches a string that has ab followed by zero or one c
- abc{2}      matches a string that has ab followed by 2 c
- abc{2,}     matches a string that has ab followed by 2 or more c
- abc{2,5}    matches a string that has ab followed by 2 up to 5 c
- a(bc)*      matches a string that has a followed by zero or more copies of the sequence bc
- a(bc){2,5}  matches a string that has a followed by 2 up to 5 copies of the sequence bc


### OR Operator

A "|" is used to as an OR operator in the JavaScript regex. If multiple patterns are being searched, can be seperated with the |
- a(b|c)     matches a string that has a followed by b or c (and captures b or c)
- a[bc]      same as previous, but without capturing b or c

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
- \d matches a single character that is a digit
- \w matches a word character (alphanumeric character plus underscore)
- \s matches a whitespace character (includes tabs and line breaks)
- .  matches any character

 ### Flags

 Flags are to specify  allowed parameters within a search. 
s  - allows a dot to act as a newline character.
i  - specifies case does not matter for the characters used in the pattern.
m  - traverses multiple lines of a queried string.
y  - searches the exact position of the pattern.
g  - returns all instances of the pattern, instead of just the first.
u  - allows Unicode support.

 - i  With this flag the search is case-insensitive: no difference between A and a.
- g  With this flag the search looks for all matches, without it – only the first match is.returned.
- m  Multiline mode.
- s  Enables “dotall” mode, that allows a dot . to match newline character \n.
- u  Enables full Unicode support. The flag enables correct processing of surrogate pairs.
- y  “Sticky” mode: searching at the exact position in the text.
 ### Grouping and Capturing

Capturing groups are a way to treat multiple characters as a single unit. They are created by placing the characters to be grouped inside a set of parentheses. For example, the regular expression (dog) creates a single group containing the letters "d" "o" and "g". The portion of the input string that matches the capturing group will be saved in memory for later recall via backreferences

 ### Bracket Expressions

 Bracket expressions simply reference the form-factor of the grouping characters. 
 - [ ] Brackets indicate a set of characters to match. Any individual character between the brackets will match, and you can also use a hyphen to define a set
- You can use the ^ metacharacter to negate what is between the brackets.
- { } Curly braces are used to specify an exact amount of things to match.
- ( ) Parentheses represent remembered matches. This is especially useful for find-and-replace operations or any time you need to do something with part of the match.
- Parentheses are also used in regex to group parts of the expression together into subgroups, like in /(\$|¥)([0-9]+)\.([0-9]{2})/.


 ### Greedy and Lazy Match

By default the regular expression engine tries to repeat the quantified character as many times as possible. For instance, \d+ consumes all possible digits. When it becomes impossible to consume more (no more digits or string end), then it continues to match the rest of the pattern. If there’s no match then it decreases the number of repetitions (backtracks) and tries again.

Enabled by the question mark ? after the quantifier. The regex engine tries to match the rest of the pattern before each repetition of the quantified character.
 ### Boundaries

The boundary operator \b  searches word positioning.
The (\b) is an anchor like the caret (^) and the dollar sign ($). It matches a position that is called a “word boundary”. The word boundary match is zero-length.
Between two characters in a string if one is a word character and the other is not.
After the last character in a string if the last character is a word character.
Before the first character in a string if the first character is a word character.

Simply put, the word boundary \b allows you to carry the match the whole word using a regular expression in the following form below.

\bword\b


 ### Back-references

 Back-references is used to store found value and group items found in between those symbols/named instances. 

 Backreferences match the same text as previously matched by a capturing group. Suppose you want to match a pair of opening and closing HTML tags, and the text in between. By putting the opening tag into a backreference, we can reuse the name of the tag for the closing tag.
  Here’s how: 
  <([A-Z][A-Z0-9]*)\b[^>]*>.*?</\1>.
This regex contains only one pair of parentheses, which capture the string matched by
 [A-Z][A-Z0-9]*.
  This is the opening HTML tag. "Since HTML tags are case insensitive, this regex requires case insensitive matching". The backreference "\1" references the first capturing group.
  "\1" matches the exact same text that was matched by the first capturing group. The "/" before it is a literal character. It is simply the forward slash in the closing HTML tag that we are trying to match.


 ### Look-ahead and Look-behind

Look-ahead allows to add a condition for “what follows”.
Look-behind is similar, but it looks behind. That is, it allows to match a pattern only if there’s something before it.

The syntax is:

- Positive lookbehind: (?<=Y)X, matches X, but only if there’s Y before it.
- Negative lookbehind: (?<!Y)X, matches X, but only if there’s no Y before it.

The syntax is:

- X(?=Y)```, it means "look for X, but match only if followed by Y". There may be any pattern instead of X and Y.
 ## Author

 [Joel A Rivera Rivera](https://github.com/Jrivera239)
 
 I have commited myself to become a fullstack developer. I have choosen different careers in my life but never been as determine as I have with developer. I currenty reside in Kissimmee, Florida and am absolutely willing to relocate for a greater future in life. I'm a dedicated individual who pursuits goals and this is a goal of mine with many more to accomplish.