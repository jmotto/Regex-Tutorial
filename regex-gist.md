# Tutorial: Regex Matching an Email

Regular Expressions (Regex) are a string of characters that define a search pattern to help easily manage data. This tutorial will explore using regex for matching an email address. 

## Summary

This tutorial will breakdown and describe the different parts of the regex used to match emails using the following expression: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ . Using matching an email regex can be useful for validating email addresses using forms and certain programs. 

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

Anchors match a position before, after or between characters. The anchors in the regular expression for matching an email are the carret ^ and the dollar symbol, $. The ^ matches the beginning of the text, and the $ matches the end of the text. In this regex the ^ and $ mark the parameters of the regex. 

### Quantifiers

Quantifiers identify how many instances of a character, group, or character class must be present in the input for a match to be found. In the regex for matching email, the + operator acts as the qualifier which will look for one or more instances of everything in brackets. 

The {2,6} also acts as a qualifier, which matches between 2-6 characters. In the case of an email address, this would identify the domain extension, such as, .com or .org at the end of an email address. 

### Grouping Constructs

Grouping constructs separate the expression into subgroups and capture the substrings of an input string. Parentheses () are used for grouping parts of the expression together. In the snippet for email matching there are three groups captured. The first subgroup is ([a-z0-9_\.-]+) which matches the email username. The next subgroup is ([\da-z\.-]+) which matches the domain name or mail server. Then the last subgroup, ([a-z\.]{2,6}), captures the top-level domain, such as .com or .org.

### Bracket Expressions

A bracket expression is a set of characters enclosed by square brackets [] which allows for matching specific characters. Let's breakdown the bracket expressions in this snippet:

For [a-z0-9_\.-], [a-z] matches any letters from 'a' to 'z' (case sensitive). [0-9] matches any number between '0' to '9'. [_\.-] matches the characters "_", "-", and "."

For [\da-z\.-], [\d] matches any digital character from '0' to '9'. Again, [a-z] matches any letters from a to z (case sensitive). [\.-] matches the characters "_", "-", and "."

For [a-z\.], this is looking for any character between 'a' to 'z' and '.'

### Character Classes

A character class matches any symbol from a certain character set. For example, the character class in this regex is the digit character class: \d , which matches any single digit between 0 to 9.

### The OR Operator

### Flags


### Character Escapes

Character escapes are used when a character is needed to be used literally and are shown by a backslash \ . 



## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
