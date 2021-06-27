# Regex- URL matching

Regex (short for regular expressions) define specific search patterns though a sequence of characters. These search patterns can help validate inputs by find patterns in strings and/or the ability to replace characters/sequences in that string.

## Summary

This tutorial will look at using strings to match URL. 

Example of matching an HTML tag we will breakdwon below:
```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
- [Refrences](#refrences)

## Regex Components

### Anchors
Anchors are the symbols are used to start and end your search expression, all the "action" will happen inside of these symbols. The below characters are used to match the relative position on a string (but will not match any characters). 
 * `^` : Beginning of input
 * `$` : End of a input string 

 Ref:
 * `/^...$/` : denotes the beginning and end of the regex expression

### Quantifiers
Quantifiers specify how to match a string to its proceeding character (or string if defined). 

Symbols with Refrences: 
* `?` : matching to the previous character is optional
    * `https?` : matches (https), (http)
* `+` : match to one or more of the proceeding character
    * `[\da-z\.-]+` : matches a single character (d), (.), (-) or group of letters (a-z) 1 or more times
* `*` : match zero or more of the previous character (combination of `?` and `+`)
    * `([\/\w \.-]*)*` : matches (/) or (//), (w) or (www), (.), (-)
* `{}` : defines how many characters will be searched for
    * `{n}` : n = the total number of characters
    * `{n, }` : n = minimum number of characters being searched for
    * `{n,m}` : m = max number of characters being searched for, n = minimum number of characters being searched for
    * `[a-z\.]{2,6}` : matches 2 - 6 copies of sequence [a-z\.]

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

### Refrences
* https://www.youtube.com/watch?v=rhzKDrUiJVk&t=26s
* https://gist.github.com/penaone/80f920d38f55e552ce1063e890a2050b



## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

Github site: https://github.com/Patelso9

About: 
