# Title (replace with your title)

Regex Tutorial

## Summary

We will be using this tutorial to discover how various components of regex can be used for certain applications. In this example, we will be learning how to validate an email that follows the corret format.

Matching an Email – /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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

### Anchors

An acnhor starts and ends the regular expression (regex.) In the code we are presented with:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

^ and $ serve as the anchors. This means that in our code, we are looking for something starting with:

^([a-z0-9_\.-]+)

by that same metric, we are also looking for something ending with:

.([a-z\.]{2,6})$ 

The password we are searching for must follow in those paramters, or else it is not a match.

### Quantifiers

A quantifier determines how many times a specific chracter or group of characters must exist in order to be a match. One example would be, if we used abc+ then we would match a string ab followed by at least one c. In the code we have:

([a-z0-9_\.-]+)

we would have a match with any string that has a-z, 0-9, _, ., or -. The quantifier, being +, means that it must have at least one of these in order to be a match.

### OR Operator

Take this hypothetical code (note, this is NOT the code we are working with:)

//#?([a-g0-9]{6}|[a-g0-9]{3})$/

This is line of hypothetical code does contain an OR operator. This means that it will match where it starts with #, which must comes first followed by either

[a-g0-9]{6} which matches a 6 character length string that contains a both a-g letters and 0-9 numbers

| OR operator

[a-g0-9]{3} which matches a 3 character length string that contains both a-g letters and 0-9 numbers

### Character Classes
When we look at our code:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

We see that \d is present, and that in turn will match a character letter, in this case a-z, after the @ in rhe email and not a number or special character.

### Flags

Our code does not contain a regex class. A regular expression typically comes in the form of

/regex/

The slashes here indicate where the regular expression starts and ends. A flag can be used to give more guidelines for matching. The flags in question are:

g which stands for 'global' and allows matching the instances in a string that follow the matching guidelines set in the regular expression,

m which stands for 'multiline' which searches line by line instead of a string as a whole.

i which stands for 'insensitive' which removes the need for the expression to be case sensitive, meaning either lower or uppercase letters could be considered matching. 

### Grouping and Capturing
Going back to our presented code: 

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

we can divide these into grouping and capturing. 

([a-z0-9_\.-]+) is the first group in our code, ([\da-z\.-]+) the second, and ([a-z\.]{2,6}) the third. We must make sure that we are matching the guidelines of each group we inspect before we move on to the next.

### Bracket Expressions

We look at our code once more:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Here we take whatever is in a set of brackets, such as 

[a-z0-9_\.-]

We look at these guidelines, which mean it can contain either letters a-z, 0-9, an underscore, a period, or a hyphen.

### Greedy and Lazy Match

The given code contains neither a greedy or lazy match

### Boundaries

In a string, we would be looking for specific words, however our code does not contain any boundaries.

### Back-references

These are not included in our given code.

### Look-ahead and Look-behind

If these are used, they must be in a specific order, however they are not present in our given code.

## Author

This was authored by Pablo Estrada, a student at Rutgers University Fullstack Coding Bootcamp.

Talk to me (Pablo Estrada)

https://github.com/Pestrada24

www.linkedin.com/in/pabloestrada24
