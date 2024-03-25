# Regex Tutorial

Regualar Expressions are a set of special characters that define a search pattern. We often times use regex when creating sensitive information or storing said information. Regex expressions have eight different components to them that selects the special characters in a sequence. In this tutorial, I will be explaining a regex expressions and breaking it down into its components to explain what the code is doing.

## Summary

Below is the following regex expression I will be going into detail:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This expression is for matching an email and we can break this regex code down to its compenents. 

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

Anchor charatcers are used to signify the beginning charatcers and ending characters or a string. The ^ anchor is used to show the starting charatcers in a string and the $ anchor is used to define the ending charatcers in a string. For this email example, the ^ shows that in the following capturing group ([a-z0-9_\.-]+) our email will being with lowercase alphabet (a-z), numbers (0-9), and an underscore with a period charatcer and a hyphen (_\.-). The $ at the end will choose the ending charatcers for the email defined by the string ([a-z\.]{2,6}). Meaning the email will end with the characters a-z following a period character with \.

### Quantifiers

Quantifiers set the limits of a regex expressions and match the occurences of a particular pattern that is not produced. For the example above, the + signs at the end of our [] brackets and the {2,6} curly brackets at the end are quatifiers. Each plus sign will match the amount times a pattern appears so it will find matching occurences for [a-z0-9_\.-] and [\da-z\.-] 1 or more times. For the {2,6} shows the minimum and maximum amount of charatcers that the final string [a-z\.] can have.

### Grouping Constructs

Grouping Constructs are used to break up the expressions into parts. They are primarily defined by () and contain the subexpressions we are looking for. In this example, we have three grouping contructs: ([a-z0-9_\.-]+), ([\da-z\.-]+), ([a-z\.]{2,6}) meaning our email has three different strings. The first two contructs are separated by the @ symbol and the last two are separated by \. or a period character. 

### Bracket Expressions

Brackets show the range of charatcers that can be matched in an expression. They are also known as positive charatcer groups as they outline the charatcers we want to include. Our brackets in this example are [a-z0-9_\.-], [\da-z\.-], and [a-z\.]. The first bracket will match lower case letters, numbers, with an underscore or hyphen spearated by a period. the second bracket will find a number between 0-9 defined by the \d and then find a lowercase letter a-z followed by a period and a hyphen. The final bracket will look for only lowercase letters.

### Character Classes

Character classes define the set of charatcers that can appera in a string. Bracket expressions are also another form of character classes. The other character class that is shown that is not a bracket is the \d. This chooses any alphanumeric digit and is the same as [0-9]. 

### The OR Operator

The or operator (|) would allow an expressions to select between different characters in regex. Since brackets do this logic already, the or operator is mainly used inside of parentheses for multiple options of charatcers. This example above does not use the or operator. 

### Flags

Flags are placed at the end of a regex expression and set additional functionality or limits in our expression. The example above does not have any flags. 

### Character Escapes

Chartcer escapes make it so that a charatcer is not interpreted literally. These are charatrcers usually have a (\) preceding them. In the example above the \. in between the two strings ([\da-z\.-]+)\.([a-z\.]{2,6}) would be an escape. This means that there will always be a period inserted between these two strings when the expressions is calculated. 

## Author

This gist document was created by Devin Belle. 