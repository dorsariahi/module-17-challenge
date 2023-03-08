# Regex Tutorial

## Summary

Today, I'll go through and dissect the components of a regular expression used to match Hex Values. Hexadecimal coding is a way for correctly describing any unique color to a computer, providing consistency and accuracy in an electronic display. A hexadecimal color value is a six-digit code preceded by a # symbol that determines the color of a website or computer software. /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ 

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
Regex will seek for anything using a variety of formulas.
[]Anything between the brackets denotes a range. For example, [abc] instructs the regex to look for strings that contain a, b, or c. [a-z] instructs the code to look for any lowercase letter between a and z.
{}Everything within the curly braces denotes regex match limitations, such as maximum or minimum length.
() Anything included in parentheses will seek an exact match based on the sequence in which the characters are shown. By grouping portions together, it may also divide our regex formula into subexpressions.
\ A backslash will allow a character that would otherwise be interpreted literally to escape. For example, [.] instructs the algorithm to match a period rather than a universal quantifier, as we shall see later.

### Anchors
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
The code will frequently start and conclude with an anchor. The anchors used in our example are and $.
The indicates that the string we're looking for starts with whatever comes after.
The $ symbol indicates that the string we're looking for terminates with the characters that come before it.

### Quantifiers
Quantifiers define the string's bounds for your intended regex match. Specifically, the maximum and lowest number of characters desired for your search.
There are broad methods to signal this, but there are other ways to narrow the search.
Generalized 1. The asterisk (*) indicates to the regex that the previous character should be gathered zero or more times. 2. The plus symbol (+) instructs the regex to collect the previous character one or more times. 2. A question mark (?) instructs the regex to gather the previous character zero or once.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ 

In both our first and second parts of code, the plus symbol is employed. It comes after our brackets and says that at least one or more characters must be present for the search to match.

Specific Our algorithm may be instructed to discover a more precise amount by using the. Here are three applications for this. 1. "n": precisely n times match 2. "n,": matches n times or more 3. "n,x": matches n times minimum and x times maximum.

In our most recent section of code, the number "2,6" is utilized. This instructs the computer code to search for a string of letters that is 2 to 6 characters long.

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
