# Reg Ex Email Matching Gist

## Summary

This is a gist about the following email matching regex:

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

This regex determines if an input is an email by first ensuring that there is a string of letters and numbers proceddign the @, then another after the @, followed by a period then a two to six character domain or domain extension.

## Table of Contents

- [Assertions](#assertions)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Assertions

Assertions include boundaries and denote the beginning and ending of an input.  This notation indicates an beginning:

```
/^
```

This notation indicates an ending:

```
$/
```

### Quantifiers

Quantifiers determine the number of characters to match.  For example, in the email match regex:

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

the expression:

```
{2,6}
```

indicates that the characters that follow the period must be at least two characters and no more than six characters long.

### Character Classes

Character classes determine the type of input the regex is looking to match.  For example in the email match regex:

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
the expression:

```
a-z0-9_
```
and:

```
\da-z
```
indicate that the regex is looking to match any and all numbers 0-9 and letters a-z while the first iteration of this character class also includes an underscore as an acceptable input type to match.

### Bracket Expressions

Bracket expressions indicdate that the regex should match based on either a single type of input or a range of types of inputs as described above in the character classes.  For example in the email match regex:

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
the expression:

```
[a-z0-9_\.-]
```

this bracket expression indicates that the regex will match all values from a-z, 0-9, and underscores before exiting to match the next portion of the expression, which is the @ outside of the first set of parenthesis.


## Author

https://github.com/tuckerreiland

