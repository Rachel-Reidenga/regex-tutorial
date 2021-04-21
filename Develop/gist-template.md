# Regex Tutorial

Regex or Regular Expression is defined as a sequence of characters that specifies a search pattern. Usually such patterns are used by string-searching algorithms for "find" or "find and replace" operations on strings, or for input validation. It is a technique developed in theoretical computer science and formal language theory.

## Summary

In this tutorial we will be covering the Components of Regex. At first Regex might look confusing and may sound a little intimidating, but once gaining a basic understanding of the Regex syntax it becomes a very useful tool for most programming languages. By the end of this tutorial we'll be able to identify the different components that make up a regex and break down a (BLANK----) regular expression.

## Table of Contents

- [Regex Tutorial](#regex-tutorial)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
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
  - [Author](#author)

## Regex Components

### Anchors
Anchors belong to the family of regex tokens that don't match any characters, but that assert something about the string or the matching process. Anchors assert that the engine's current position in the string matches a well-determined location: for instance, the beginning of the string, or the end of a line.

^ marks the beginning of a string
$ marks the end of a string
\A marks the beginning of string
\z marks the end of string

The caret anchor ^ asserts that the engine's current position in the string is the beginning of the string. Therefore, ^r matches a r at the beginning of the string.

### Quantifiers
Qunatifiers are characters within the regular expression that specify how many instances a character, group, or character class must be represented in the input to be matched. Any regular expression element can be qualified by one of the following three characters: *, +, or ?.

* The Qualifying Character: * matches 0 or more occurrences of the element that procedes it. An example of this is:
cat_[a-z0-9]* matches: cat_5 , cat_abc , cat_z26 because cat_ is followed by 0 or more alphanumeric values.

* The Qualifying Character + matches 1 or more occurrences of the element it follows. An example is:
cat_[a-z0-9]+ matches cat_5 , cat_abc , cat_z26 becasue cat_ is followed by 1 or more alphanumeric values.
cat_[a-z9-0]+ dose NOT match cat_ because it is NOT followed by any alphanumeric values.

* The Qualifying Character ? matches 0 or 1 occurrences of the element it follows. An example is:
cat_[a-z0-9]? matches: cat_0 , cat_ , cat_a , cat_ zz because cat_ is followed by 0 or 1 alphanumeric values.

### OR Operator
OR Operators (Alternation Operator) matches on of a choice of regular expressions: if you put the character(s) representing the alternation operator between any two characters in the regular expression, the result matches the union of the strings that those two characters match. Okay, that was kind of a lot so lets break it down.

* [] matches any single character in the range within the brackest. An example is:
  [aeiou] matches any vowel.

* | Is an OR Operator. Example being:
  cat|dog will find cat OR dog.


### Character Classes
Character Classes tells the regex engine to match only one out of multiple specific characters, such as words, numbers or whitespace. 

* \d matches a single character that is a digit
* \w matches a word character (any alphanumeric character plus underscore)
* \s matches a whitespace character (including tabs and line brakes)
* . matches any character
  
The capital case for any aformentioned characters will inverse the match

* \D matches a single non-digit character
* \W matches a single any non-character that is a-z
* \S matches a single non-whitespace character

Square brackets are used to specify character classes (also known as character sets). For example:

* The regular expression [Cc]at means: an uppercase C or lowercase c, followed by the letter a, followed by the letter t.
  '[Cc]at' --> The big 'Cat' sat next to the small 'cat'.


### Flags
Flags are optional parameters that can be added to a plain expression to make it search in a different way. Flags are also called modifiers because they modify the output of a regular expression. These flags can be used in any order or combination, and are an integral part of the RegExp. Each flag is denoted by a single alphabetic character, and serves different purposes in modifying the expression's searching behavior.

* g Global search, does not return after the first match, which restarted any subsequest searches from the end of the previous match Therefore making the expression search for all occurences.
* m  Multi-line search when enabled the Anchors (^ $) will match the start and end of a line, rather than the whole string
* i Insensitive search makes the entire expression case-insensitive

So by using these Flags:

/Cat/g   matches all `Cat` in the test
/Cat/m   matches the beginning and ending of each line with `Cat`, rather than the whole string `Cat` itself
/Cat/i   matches all `Cat` because it is case-insensitive so Cat, cAt, caT, cat, CAT, all match.



### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
