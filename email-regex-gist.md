# Email Regex Tutorial

Regular expression for an email that verifies if a string is an email.

## Summary

'/^([a-z0-9_\\.-]+)@([\da-z\\.-]+)\\.([a-z\\.]{2,6})$/' This is the regex that can validate an email, it does so by grouping 3 parts. the username(anything before the '@'), domain name, and TLD(.com, .net, .org, etc.) verifying wheter they fit the bracketed criteria.

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
/^([a-z0-9_\\.-]+)@([\da-z\\.-]+)\\.([a-z\\.]{2,6})$/

### Anchors

* /<mark>^</mark>([a-z0-9_\\.-]+)@([\da-z\\.-]+)\\.([a-z\\.]{2,6})<mark>$</mark>/

* Start and end of the regex: 
    * '^' - start of expression
    * '$' - end of expresssion


### Quantifiers 

* /^([a-z0-9_\\.-]<mark>+</mark>)@([\da-z\\.-]<mark>+</mark>)\\.([a-z\\.]<mark>{2,6}</mark>)$/

    * '+' - matches elements past the first characters(without '+', it would only scan up to the first characters)
    * '{2,6}' - will only accept characters 2 - 6 characters in length


### Grouping Constructs

* /^<mark>([a-z0-9_\\.-]+)</mark>@<mark>([\da-z\\.-]+)</mark>\\.<mark>([a-z\\.]{2,6})</mark>$/

    * '([a-z0-9_\.-]+)' - this groups the username before the @
    * '([\da-z\.-]+)' - this groups the domain name
    * '([a-z\.]{2,6})' - this groups the TLD(.com, .net, .org, etc.)
    

### Bracket Expressions

* /^(<mark>[a-z0-9_\\.-]</mark>+)@(<mark>[\da-z\\.-]</mark>+)\\.(<mark>[a-z\\.]</mark>{2,6})$/
    * '[a-z0-9_\\.-]'
        * 'a-z' - allows any lowercase letter from a - z
        * '0-9' - allows digits 0-9
        * '_' - allows underscores
        * '\\.' - allows dots
        * '-' - allows hyphens
    * '[\\da-z\\.-]'
        * '\d' - allows digits 0-9
        * 'a-z' - allows any lowercase letter from a - z
        * '\\.' - allows dots
        * '-' - allows hyphens

### Character Classes

* /^([a-z0-9_\\.-]+)@([<mark>\d</mark>a-z\\.-]+)\\.([a-z\\.]{2,6})$/
    * '\d' allows numbers 0 - 9

### The OR Operator
* N/A

### Flags
* N/A

### Character Escapes

* /^([a-z0-9_<mark>\\.</mark>-]+)@([\da-z<mark>\\.</mark>-]+)<mark>\\.</mark>([a-z<mark>\\.</mark>]{2,6})$/
    * '\\.' this character escpae is used to allow a dot


## Author

Github: https://github.com/jensenjamessaoit
