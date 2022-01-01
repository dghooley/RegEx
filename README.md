# Regex Tutorial: Computer Science for JavaScript Challenge

This is a brief, concise tutorial explaining Regular Expressions or "Regex" (also referred to as a 'rational expression'). A Regex is a sequence of special, unique characters that are utilized to specify a search pattern. Typically, these patterns are used by string-searching algorithms (in JavaScript regular expressions are also objects) for input validation and are commonly found in search enignes, word processors and text editors. Because they have uses in many programming languages, they are an important component of theoretical computer science. 

## Summary

In this tutorial, we will cover this Regex for email:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

We will break down the components that make up this pattern of characters and how they are used to perform pattern-matching or "search-and-replace" functions on text.


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors

Anchors are unique in that they do not match a literal character. Instead, they mark a position before, after, or between characters. The caret anchor `/^` marks the beginning fo the string being searched and conversely, the dollar anchor `$/`  `([a-z\.]{2,6})$/` marks the end of the string. `\A` marks the beginning of a string, and `\z` marks the end. There are variations between search engines and languages and which character is supported, so it's best practice to double check before using them. 

### Quantifiers

Quantifiers are used to define the number of characters in the RegEx. In the aforementioned code, the quantifier `{}` would be used at the end of the email (.com, .net, .edu) when searching for letters and a period. `([a-z\.]{2,6})$/`

### OR Operator

Also referred to as Union or Alternation Operator, the OR operator is identified by `|` . While the RegEx above for an email does not contain any of these operators, it could potentially be used to search for two specific addresses. For instance, if one were to search exclusively for '.edu' or '.com', the RegEx would resemble the following code  `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.(com|net)$/`

### Character Classes

When disginguishing between characters (i.e. letters and digits), Character Classes are utilized. `\d` Matches any digit equivalent to `[0-9]`. `/s` matches a single whitespace character (e.g. space, tab, form feed, line feed). `/t` matches a horizontal tab. 

### Flags

Using Flags in RegEx is optional, but can prove helpful when running global searches for case-sensitive patterns. `/g` is a global flag, `/i` is used to ignore casing, `/u` is unicode, and `/m` is multiline.

### Bracket Expressions

When searching for a set of characters, Bracket Expressions are used to indicate the parameters. If we were to run a search for `[.com]` , we will return everything that contains '.com'.  Similarly, if we need to serach a range of letters, we could use `[a-z]` .  All characters inside these brackets are case-sensitive. To indicate a case change, we would use the `i` flag.  `[a-z]/i`  Both numbers and characters can be used in the Bracket Expressions.

## Author

Derick Hooley 

Check out my GitHub profile here: 
https://github.com/dghooley


