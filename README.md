# Understanding the Regex for Matching URL Patterns

In this tutorial, we will explain a specific regex designed to match URL patterns. We will break down each component of the regex and discuss how it contributes to the overall search pattern. By the end of this tutorial, you will have a better understanding of how this regex works and how it can be used to find URLs in text.

## Summary

The regex we will be examining in this tutorial is designed to match simple URLs. The regex pattern is as follows:

```
^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$
```

We will explain each part of this regex in detail in the following sections.

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

In the given regex, `^` and `$` are anchors. The `^` anchor matches the start of a string, while the `$` anchor matches the end of a string. By using these anchors, we ensure that the regex matches the entire URL string and not just a part of it.

### Quantifiers

Quantifiers in this regex include `?`, `*`, and `+`. The `?` quantifier indicates that the preceding element is optional, appearing either 0 or 1 times. The `*` quantifier indicates that the preceding element can appear 0 or more times. The `+` quantifier means that the preceding element must appear 1 or more times.

### OR Operator

The OR operator `|` is not used in this regex. However, it is important to know that the OR operator allows a regex to match either one pattern or another.

### Character Classes

Character classes are represented by brackets `[]` and indicate a set of characters that can be matched. In this regex, we have several character classes:

- `\d`: Matches any digit (0-9)
- `a-z`: Matches any lowercase letter (a-z)
- `A-Z`: Not present in this regex, but matches any uppercase letter (A-Z)
- `\.`: Matches a period (.)
- `\w`: Matches any word character (alphanumeric or underscore)

### Flags

There are no flags in this regex. Flags are used to change the behavior of the regex pattern, such as making the pattern case-insensitive or enabling multiline mode.

### Grouping and Capturing

Grouping and capturing are represented by parentheses `()`. In this regex, we have several groups:

1. `(https?:\/\/)`: This group matches the URL's protocol (http or https) followed by `://`. The `?` quantifier makes this group optional, allowing for URLs without a protocol.
2. `([\da-z\.-]+)`: This group matches the domain name, which can consist of digits, lowercase letters, periods, and hyphens.
3. `([a-z\.]{2,6})`: This group matches the top-level domain, which can have 2 to 6 lowercase letters and periods.
4. `([\/\w \.-]*)`: This group matches the URL path, which can include forward slashes, word characters, spaces, periods, and hyphens. The `*` quantifier allows this group to appear 0 or more times, making it optional and accommodating URLs without a path.

### Bracket Expressions

Bracket expressions are used to define a custom character class. In this regex, we have several bracket expressions:

- `[\/\w \.-]`: This bracket expression matches forward slashes, word characters, spaces, periods, and hyphens, which are allowed in the URL path.

### Greedy and Lazy Match

There are no specific greedy or lazy quantifiers in this regex. By default, quantifiers like `*`, `+`, and `?` are greedy, meaning they will match as many characters as possible. To make them lazy, you can add a `?` after the quantifier, making them match as few characters as possible.

### Boundaries

There are no word or character boundaries in this regex. Boundaries are denoted by `\b` and are used to assert the position between a word character (alphanumeric or underscore) and a non-word character. They can be helpful when trying to match whole words or phrases.

### Back-references

This regex does not use back-references. Back-references allow you to refer back to a previously captured group within the same regex pattern. They are denoted by `\1`, `\2`, etc., where the number corresponds to the order of the capturing group.

### Look-ahead and Look-behind

Look-ahead and look-behind assertions are not used in this regex. These assertions check for a pattern before or after the current position without consuming any characters. Look-aheads are denoted by `(?=...)` for positive look-aheads and `(?!...)` for negative look-aheads. Look-behinds are denoted by `(?<=...)` for positive look-behinds and `(?<!...)` for negative look-behinds.

## Author

This tutorial was created by [Edson Petry](https://github.com/EdsonPetry)
