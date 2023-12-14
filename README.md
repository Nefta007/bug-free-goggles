# HEX Value REGEX Tutorial;

This tutorial will go into detail braking down the process of interpretting a regex expression. In this case we will loook at a HEX value

## Summary

This tutorial will show the way in which to decode a Regex which is short for Regular Expression. We will be looking at the expression `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/` and taking apart its various components.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)


## Regex Components
As you can see the `/` is present at the both ends of the expressiong. This is because they serve as a sort of container for the expression. 
### Anchors
When looking for anchors you are identifying the `^` and `$` characters. the `^` is used to signify a string that begins with the following characters and the `$` tells us that whatever characters is in front of it will be at the end of the string. From our expression we see that following the `^` the hashtag follows meaning that the string we are looking for will start with the hashtag. We also see that our string will end with the characters a to f and 0 to 9.

### Quantifiers
Quantifiers set the limit of the string and can set both a max and a min amount of characters in the string. Quantifiers can be a little tricky, if we take a look at {n}, this will set the limit to exactly n. Add a comma after the n: {n,} you now have it saying at least the amount of n and finally you have {n,m} this sets your limit to a minimum of n and a max of m. From our expression we see that there are two quantifiers, one setting up a limit of exactly 6 charcters and another one setting up an exact amount of 3. we also have the ? which means that the patter maches an amount of zero or one time. The following characters is the legend for what each quantifier means:
 - `*` patter matches 0 or more times
 - `+` patter matches 1 or more times
 - `?` patter matches 0 or 1 time
 - `{}` as  stated above this will set your limit

### OR Operator
The or operator will make the expression go from abc to a or b or c meaning anyone of those characters can be fond but not all of them. So in our case we see that our expression will have a combination of 6 characters a to f 0 to 9 or 3 characters a to f 0 to 9
### Character Classes
Character classes will define a set of characters which can occur in a string to fulfill a match.  We also don't have to know this however also doesn't hurt to know. Most common are as followed:
 - `.` this will matach any character except newline
 - `\d` this will match any arabic numeric digit
 - `\w` this will match any alphanumeric character from basic latin alphabet
 - `\s` this will match a single whitespace character including tab and line break
### Flags
Flags represents additional functionality, in our case we don't have to worry about it but it does not hurt to know the following legend. We also don't have to know this however also doesn't hurt to know
 - `g` Is global search. this will test against all possible matches
 - `i` This means it is case insensitive searches.
 - `m` This is Multi-line search

### Grouping and Capturing
The `()` will group sections of the expression together. This is mostly used when the expression grows too complicated and you want to check multiple parts of the string. So the `()` will check for the different sections. In our case we are searching for the `#` and for `[a-f0-9]{6}|[a-f0-9]{3}`

### Bracket Expressions
The brackets in expression will represents ranges of characters that we want to match. In our case we are looking from characters that range from a to f and from 0 to 9

## Author
Neftali Percastegui https://github.com/Nefta007