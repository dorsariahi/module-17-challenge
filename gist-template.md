# Regex Tutorial

## Summary

Today, I'll go through and dissect the components of a regular expression used to match Hex Values. Hexadecimal coding is a way for correctly describing any unique color to a computer, providing consistency and accuracy in an electronic display. A hexadecimal color value is a six-digit code preceded by a # symbol that determines the color of a website or computer software. /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping](#grouping)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

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
Although it is not utilized in our code, the OR operator functions similarly to the OR function in JavaScript.

A | tells the regex formula that either/or characters are a match when it is placed between two characters inside of brackets.

### Character Classes
A group of characters are defined by character classes. These are some examples.

* . matches any character aside from \n
* \d matches any digit 
* \w matches any alphanumerical character
* \s matches a single whitespace

### Flags
Capitalizing the letter will find the inverse of the desired method.

We see this used used multiple times in our regex formula. 

 /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

The first instance where this is used is the \d in our second segment. This tells the regex to look for any digit in the string.
Notice that the . is not considered a class in the first segment of code. This is because the backslash indicates that we are looking for a literal period instead of any character.

### Grouping
As previously indicated, we may use parentheses to separate our regex into subexpressions. In our code, this is done three times. Secondly, we will divide our desired action into three components.

1. Email Name
([a-z0-9_\.-]+)

2. Domain
([\da-z\.-]+)

3. Extension
([a-z\.]{2,6})
Between these groups we see the literal characters @ and . (a regular period), these tell the regex to look for exactly those characters between our other specified instructions.

### Bracket Expressions
The brackets once again represent a range of characters to look for. Let's explore what these mean within our code.
1. Email Name
([a-z0-9_\.-]+) 
    - The first portion says a-z, meaning it's searching for any lowercased letter. 
    - The second portion says 0-9, this searches for any number within that range.
    - The _ and - indicate that these are both valid characters to search for.
    - As stated before, \. indicates that a period is a valid character to search for.
    - Finally, the + outside the bracket implies that there must be at least one character for this to be a valid search. 

2. Domain
([\da-z\.-]+)
    - The first portion \d indicates that it is looking for any digit. This is similar to 0-9.
    - The second portion is the same as above, a-z, searching for any lower cased letter.
    - Next we have the two special characters that are matches, . and -
    - Similar to above, + implies that there must be at least one character for this to be a valid search. 

3. Extension
([a-z\.]{2,6})
    - The first portion a-z searches for any lower cased number.
    - The second portion that . will be a match.
    - Lastly, we have an expression within {}. This signifies that the final block can only have from 2 to 6 characters. 

### Greedy and Lazy Match
Regex is viewed as a system that is greedy. It will thus search for as many possibilities to use the specified string as it can. To avoid this, we can utilize certain symbols.

A ? can be added after a quantifier to indicate to match as few times as possible. 

## Author
If you have any questions you can contact me at my email, dorsariahiasl@gmail.com take a look at my most recent projects at www.github.com/dorsariahi
