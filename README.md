# Explaining-Matching-URL-Regrex
# A simpltons guide to using and knowing how to use Matching URL Regrex

A Regrex is a sequence of Characters to define a specific pattern to use in a search. This regrex, sequence of patterns to search for, will be looking for a matching URL.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

The regrex seen above simply asks one thing:
-is the following or given question a valid URL? or is it not?

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components
The following will break down what this regrex does, its individual components and it will help us better understand how to use it.

### Anchors
There are two principle "anchors" in this regrex. They constitute the BEGINNING and the END of the string that will be used to search for any matches. The beginning is marked by the "^", and tells the regrex to look for any matches to the string that immedietly follows "^". The end is marked by a "$" so this tell sthe regrex that any BEFORE this "$" is in the marked search and to not use any code that follows.

### Quantifiers
First let us identify what a quantifer IS. These are use dto define how many times, in number form, a given expression may or is going to identified. Quantifiers are the following: "?", "*" and "{}" . "?" makes a single instance of the character preceding the quanifier optional. "*" represents that the preceding characters may be used in multiple instances and "{}" defines the RANGE of what possible instances may be identified.

(https?:\/\/)?

Note above, the "?" is used twice, first to show that the "HTTP" is going to be used once, and then following is the second "?" to show that all code in the " () " is going to be used once. The regrex will then now to look for "HTTP://" OR "HTTPS://" once and then whatever comes after once as well.

([\/\w \.-]*)*\/?$/

Note above that the "*" is used to show that each sequence of code may be used more than once.

### OR Operator and Bracket Expressions
([\/\w \.-]*)*\/?$/

Note above that the following "[]" is used. These are used for the search to look for any characters or any character classes that match the expression that is included in the "[]". So in the expression above, the seach will look for anything with "\w" or anything between "a-z" OR any "\." OR any "-".

### Character Classes
There are two used in the URL matching regrex. The first is "\w" and this willl look for any alphanumeric character and the other is "\d" and this will look for any chracter class with a digit. (so the d is for digit? I think so.)

### Flags


### Grouping and Capturing
Grouping is used to check multiple parts and sections of a string or multiple strings for different requirements. And example is "()" this creates a sub section that will look for AN EXACT MATCH of what is outlined, nothing devieating. so for example (Your Mom):(Your mama) is being outlined in the search and it will only look for anything that is matching, so (Your Dad):(Your Daddy) will not even be considered for a match since (Your Mom):(Your mama) and Your Dad are completly seperate things.

### Bracket Expressions
For the record, these are also know as Positive Character Groups. Make sure to remember this OR ELSE things start to get VERY confusing.

Bracket Expression/Positive Character Groups are simply as follows: whatever is in the brackets is what we want matched, and matched EXACTLY!!!!

So if the bracket includes "a-z" then it will have the characters from a to z in there.
If it includes "\d" then it will have numbers in that place.
if it has "\." then it will have a dot there.
if it has "\w" then it will have alphanumeric numbers there.

And most important Bracket Expressions = Positive Character Groups AND Positive Character Groups = Braket Expressions!


## Author

Mattchief4234 is a studied artist with aspirations in programing and website design. He loves to draw almost as much as he loves to study new topics as his mind always races with thoughts such as "maybe I could make a song?" or "What if I created a website that would calculate how much damage your hunter would do based on their armor stats, weapons stats, charms and other stats in Monster Hunter World?". Many of these thoughts remain as such... Pleas visit his GitHub profile at: https://github.com/mattchief4234