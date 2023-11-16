# REGEX Tutorial

Regular Expression, also known as "Regex"; is a sequence of characters that defines a specific search pattern. Regex can be used to find certain patterns of characters within a string. Regex is most frequently used to validate inputs from a user.

## Summary

The REGEX we will be discussing is a Matching Email expression. We will deconstruct this following statement: 
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
The regex is used to verify that the user input is a valid email address. More details of this Regular Expression will be provided below

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Look-ahead](#look-ahead)

## Regex Components

### Anchors

Regex 'Anchors' are elements, or tokens, that are known to not match any characters. On the contrary, they are known to create relationships between strings and other related processes. Further, they reserve currently determined locations for strings, whether it be at the beginning or at the end of a string.

The characters (^) and ($) are both considered to be anchors.

The use of the (^) signifies the start of the search characters.

The use of ($) signifies the end of the search characters.

### Quantifiers

Quantifiers are the characters: *, +, ?, and {}. Quantifiers match the specified quantity of the previous token. So an example with the email validation, "/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/", the quantifier will match the tokens from 2 to 6 within {} and match the string with +.

### OR Operator

OR Operator are the characters: | and []. OR Operator matches the characters within the tokens. So an example with the email validation is, "/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/", The [] looks for those tokens and matches them specifically.



### Grouping and Capturing

Grouping and Capturing are the characters: (). It groups multiple tokens together to create a capture group for extracting a substring. So with the email validation, "/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/", it is capturing the group together within the parentheses.

### Bracket Expressions

Bracket expressions are composed of characters and/or character classes encompassed within brackets.

In the case of the password strength validation Regex, bracket expressions include [a-z] and [A-Z] which match any character from lowercase a through z and uppercase A through Z, respectively. The [!@#\$%\^&\*] will match any of the special characters within that set as well.

### Greedy and Lazy Match

Greedy operators are the characters: * + {}. The lazy operator is the character: ?. Greedy operators match the token to the token before. The lazy operator makes the quantifier lazy which makes it match as few characters as possible. So in the email validation, "/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/", there is no lazy operator. However, it does contain greedy operators which allows the tokens to match specifically.


### Look-ahead 

Positive look-aheads are used after a ^ anchor in order to validate a condition by triggering each look-ahead one by one at the beginning of the string.

In the case of the password strength validation Regex, the (?=.*[A-Z]) for example, matches that the password must contain at least one uppercase ASCII letter after any zero or more characters.

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

Jasmin Flores is a software developer, 
Github Profile : https://github.com/Jazzyjz
