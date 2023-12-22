# RegEX tutorial

Hello, my name is Arthur. I'm an aspiring CS student at UTSA and to deepen my understanding I will like to provide a tutorial on RegEX.

## Summary

By the end of the RegEX tutorial you'll be able to dissect the following RegEX expression:

- `^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
- [Conclusion](#conclusion)

## Regex Components

- Regex components are characters when comprised in a seqeuence, will define a search pattern. Certain characters enable certain abilities and these abilties are what we refer to as components.

### Anchors

- Anchors are charcters in regex which specify/ensure a string's position should match a search pattern. We have two characters for Anchors.

- 1. ^ : Referred to as a Caret. This characters is used at the beginning of a string to ensure that a search matches only if the specified pattern is found at the beginning of a string.

- 2. $ : Referred to as the Dollar sign. This character is used at the end of a pattern. This character ensures that a pattern is found at the end of a string.

- You'll find these characters at the start and end of the example.

### Quantifiers

- Quantifiers are characters that allow you to specify the number of instances of a character/group appear.

- 1. '*' : Referred to as an Asterisk. Which ensures a preceding character/group 0 or more times.

- 2. '+' : Referred to as a Plus sign. Which ensures a preceding character/group 1 or more times.

- 3. ? : Referred to as a Question mark. Which ensures a preceding character/group 0 or 1 time.

- 4. {} : Referred to as Curly Braces. Used to specify either a exact number or a range of numbers for a preceding character/group to appear.

### Grouping Constructs

- Grouping Constructs are characters that create a subpattern(s) within an expression.

- 1. () : Referred to as Parentheses. These characters capture a group within the Parentheses.

### Bracket Expressions

- Bracket Expressions are characters that define a set of characters. Ensuring that any character in the input string must match.

- 1. [] : known as Square Brackets. These characters ensure that any character within the square brackets are a character for which the input string must match.

### Character Classes

- Character Classes are notations that are used to simplify the pattern matching process. Some commonly used character classes are:

- 1. . : Referredto as the Dot. This matches any single character with the exception of newline characters.

- 2. \d : Referred to as the Digit. This matches any digit character (0-9).

- 3. \w : Referred to as the Word. This matches any word character which includes letters, underscores, and digits.

- 4. \s : Referred to as Whitespace. This matches any whitespace character such as tabs, newlines, spaces, etc.

### The OR Operator

- The OR operator is used to specify and alternative(s).

- 1. | : Character for the OR operator.

### Flags

- Flags are characters that alters the way the regex engine interprets a pattern.

- 1. g : Referred to as Global. Alters the regex engine to find all matches in the input string.

- 2. i : Referred to as Case Insensitive. Alters the regex engine to match letters in a case insensitive method.

### Character Escapes

- Character Escapes are a character that give other characters literal meaning. The character used for character escape(s) is below:

- 1. \ : Referred to as Backslash.

### Conclusion

Now that we have learned regex components. Lets put that knowledge together by dissecting the following regex expression:

- `^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$`

- 1. `^`: Starting from the beginning we have the Caret(^) character thats asserting a position.

- 2. `(https?:\/\/)?`: We have a captured a group of the protocol (https) where we have a quantifier which states that the 's' in https is optional. Also, ending the captured group with a quantifier. We're stating the including the entire protocol is optional.

- 3. `([\da-z\.-]+)`: This is another captured group which gives the constraints that are allowed for the domain part of the URL which is (a-z), digits, dots, and hyphens are allowed within the domain name.

- 4. `\.([a-z\.]{2,6})`: This is also constraints for the domain passed the '.'. we have a length constaint stating that there should be a minimum of 2 characters and a maximum of 6 characters after the '.'.

- 5. `([\/\w \.-]*)`: A captured group for the path of the URL, ensuring that we're able to have 0 or more of the following characters: /, word characters, spaces, dots, or hyphens.

- 6. `*`: A quantifier indicating that the aforementioned captured group can appear 0 or more times.

- 7. `\/?`: We have a quantifier that makes a trailing slash OPTIONAL.

- 8. `$`: We end it off with a ending Anchor character.

## Author

Created by:

Arthur Bridges (https://github.com/Arthur-Bridges)
