# Regex Tutorial for Matching a Hex Value

The purpose of this assignment is to familiarize myself with regular expressions and how to use them.

Regex is short for regular expression. A regex is a string of characters for describing a search pattern.

## Summary

The regex I will be explaining is how to search and match for a hex value. The code snippet for this regex is `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`.

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

- The first element of the regex is the `^` symbol. This means the pattern following must appear at the very start of the string. It ensures that the match must occur at the beginning of the input. 

- The last element of the regex is `$`. This means the pattern preceding must appear at the very end of the string. It ensures that the match must occur at the end of the input.

### Quantifiers

- The `?` is a quantifier that tells means "zero or one" of the preceding character or group. In this regex, it is saying that the `#` is optional. Meaning, the hex value may or may not have a `#` symbol in front of it since they are not always necessary.

- The `{n}` quantifier means "exactly n" of the preceding group. In the context of `[a-f0-9]{6}`, it means exactly 6 characters are either digits `0-9` or lower case letters `a` through `f`. In the context of `[a-f0-9]{3}`, it means exactly 3 characters are either digits `0-9` or lower case letters `a` through `f`.

### Grouping Constructs

- The `()` are used as the grouping constructs in this regex example. It is grouping `[a-f0-9]{6}` and `[a-f0-9]{3}` together. That way, the regex will match either exactly 6 characters from the `[a-f0-9]` or exactly 3 characters from the `[a-f0-9]` group.

### Bracket Expressions

- The `[]` are used to designate a bracket expression. The search will match anything in the brackets. In this example, they are enclosing the character classes `a-f0-9`.

### Character Classes

- A character class matches any one character from a set of character defined within the bracket expression `[]`. In this example, it is `a-f0-9`. This means to match any lowercase letter `a` through `f` and any digit `0-9`. 

### The OR Operator

- The OR operator in this regex is the `|` symbol. This means that either expression to the left or right of the symbol can be returned in a search, since they are in the same grouping construct `()`.


## Author

My name is Dominic DeCapite and I am a student in a Full Stack Coding Bootcamp. I wrote this tutorial on a hex value regex to better familiarize myself with how regexs operate and what the symbols represent. A link to my Github profile can be found [here](https://github.com/domdecap).

