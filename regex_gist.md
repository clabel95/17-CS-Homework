# Regex Tutorial: Matching a Hex Value

In this tutorial I will explain how to write a regex that can be used to match a hex value.

## Summary

In this tutorial I will be explaining how to use the following regex:


  `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
  
I will explain each of the components that this regex includes which will be broken down in the following way.

`^`  -Start anchor

`#?`  -Non-greedy match

`(`   -Grouping

`[a-f0-9]`  -Bracket with characters

`{6}` -Quantifier 

`|` -Or

`[a-f0-9]` -Bracket with characters

`{3}` -Quantifier

`)` -Grouping

`$` -Stop anchor

This regex will search for a string that may or may not have a # at the front then either 6 or 3 characters with any combination of a-f and 0-9.

The following are a few examples of string that would pass this regex.

`#aa9`

`fe429b`

`#aaa943`

`001`


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Author](#author)

## Regex Components

### Anchors
The characters **^** and **$** are anchors. Anchors are located at the begining and end of a regex.

The **^** anchor denotes the start of the regex and the **$** character denotes the end of the regex.

### Quantifiers]
Quantifiers indicate the number of characters that can be matched. In our regex the quantifiers are the following. 

`` {6} {3} ? ``

Our regex checks to see if the string is either 6 or 3 characters long and it also checks if there is a # at the begining. The ? quantifier checks to see if there is between 0 and 1 of the preceeding character. This quantifier basicly says this character may or may not be at the start of the string. 


### Grouping Constructs
Constructs can be grouped by using parenthesis. In our regex there is a single group following the # so our regex will check what is within our group.

`([a-f0-9]{6}|[a-f0-9]{3})`

### Bracket Expressions
Bracket expressions are used to mach multiple characters. Any character that is in be bracket expression will be able to match when the regex is used. 

In our example the characters are a through f and 0 through 9, so our regex checks to see if the characters are any of those and if they are then it will match.

### The OR Operator
The or opperator means the regex will either try and match whatever is on the left of the operator or what is on the right. In our case we are matching either a 6 character string of a-f and 0-9 or we are matching a 3 character string of the same characters.

## Author

I am a full stack developer from Austin, Texas. I also have a bachelors of engineering from Abilene Christian University.

You can contact me on github at [clabel95](https://github.com/clabel95)