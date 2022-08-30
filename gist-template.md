# Learn Regex

Want to learn the basics of regex then you've come to the right place friend!

## Summary

Here we will go over the basics of regex and how to use operations and other syntax within regex!

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

### Anchors

^The matches any string that starts with The
end$ matches a string that ends with end
^The end$ exact string match (starts and ends with The end)
roar matches any string that has the text roar in it

### Quantifiers

- - ? and {}
    abc* matches a string that has ab followed by zero or more c
    abc+ matches a string that has ab followed by one or more c
    abc? matches a string that has ab followed by zero or one c
    abc{2} matches a string that has ab followed by 2 c
    abc{2,} matches a string that has ab followed by 2 or more c
    abc{2,5} matches a string that has ab followed by 2 up to 5 c
    a(bc)* matches a string that has a followed by zero or more copies of the sequence bc
    a(bc){2,5} matches a string that has a followed by 2 up to 5 copies of the sequence bc

### OR Operator

| or []
a(b|c) matches a string that has a followed by b or c (and captures b or c)
a[bc] same as previous, but without capturing b or c

### Character Classes

\d \w \s and .
\d matches a single character that is a digit
\w matches a word character (alphanumeric character plus underscore)
\s matches a whitespace character (includes tabs and line breaks)
. matches any character

### Flags

A regex usually comes within this form /abc/, where the search pattern has two slash characters /. At the end we can specify a flag with these values
g (global) does not return after the first match, restarting the subsequent searches from the end of the previous match
m (multi-line) when enabled ^ and $ will match the start and end of a line, instead of the whole string
i (insensitive) makes the whole expression case-insensitive (for instance /aBc/i would match AbC)

### Grouping and Capturing

()
a(bc) parentheses create a capturing group with value bc
a(?:bc)\* using ?: we disable the capturing group
a(?<foo>bc) using ?<foo> we put a name to the group

### Bracket Expressions

[]
[abc] matches a string that has either an a or a b or a c -> is the same as a|b|c -> Try it!
[a-c] same as previous
[a-fA-F0-9] a string that represents a single hexadecimal digit, case insensitively -> Try it!
[0-9]% a string that has a character from 0 to 9 before a % sign
[^a-za-z] a string that has not a letter from a to z or from A to Z. In this case the ^ is used as negation of the expression -> Try it!

### Boundaries

\b and \B
\babc\b performs a "whole words only" search

## Author

Junior Web developer https://github.com/R31ZH
