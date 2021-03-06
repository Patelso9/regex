# Regex- URL matching

Regex (short for regular expressions) define specific search patterns though a sequence of characters. These search patterns can help validate inputs by find patterns in strings and/or the ability to replace characters/sequences in that string.

## Summary

This tutorial will look at using strings to match URL. 

Example of matching an HTML tag that will be broken down below:
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
- [Character Escapes](#character-escapes)
- [Refrences](#refrences)

## Regex Components

### Anchors
Anchors are the symbols are used to start and end your search expression, all the "action" will happen inside of these symbols. The below characters are used to match the relative position on a string. 
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

    * `[a-z\.]{2,6}` : matches 2 - 6 copies of [a-z\.]

### Grouping Constructs
`()` : Parenthesis define a group that only acts upon itself
* `(https?:\/\/)?` : can match ' ', 'https://', 'http://'
* `([\/\w \.-]*)` : can match '/', '/ab.', ' '

### Bracket Expressions
`[]` : Brackets enables the expression to search for multiple characters 
 match any of the characters in the square brackets
* `[\da-z\.-]+` : matches a single character (d), (.), (-) or group of letters (a-z) 1 or more times

### Character Classes
Set sequences of characters that match a larger set of characters:
* `[a-z]` : matches any lowercase character in the alphaget from a through z
* `\w` : matched a word
* `\d` : matches a single character that's a digit
* `.` : matches any character

### The OR Operator
` | ` : is the character is used as an OR to enable searching multiple possiblitlies
* `(t|T)he` : enables searching for 'the' or 'The'

There are no examples of the OR opperator being used in the above expression, but I am keeping it in here since I think it's an important concept.

### Character Escapes
`\` preceeds a predefined special character (see above for reference) and enables the ablility to above and be able to search for these special characters in the regex. 

Characters such as: `(` `)` `.` `[` `]` `{` `}` `/` `+` `|`

### Refrences
* https://www.youtube.com/watch?v=rhzKDrUiJVk&t=26s
* https://gist.github.com/penaone/80f920d38f55e552ce1063e890a2050b


## Author

Hi, my name is Sonali and I am a full-stack bootcamp student. I created this tutorial when learning regex by using URL matching. My github account is linked below if you want to check out more of my work.

Github site: https://github.com/Patelso9
Link to gist: https://gist.github.com/Patelso9/29f2c2794f971722cd0fb29bbf2657bc
* (gist did not set up with proper formatting)

