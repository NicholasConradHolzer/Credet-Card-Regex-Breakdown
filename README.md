# Credit Card Regular Expressions

Introductory paragraph (replace this with your text)

## Summary

The Regular Expresion (Regex) I will be discussing will be the regex for credit card-number digital-input.  The regular expression string for this form of data:

	"   ^(?:4[0-9]{12}(?:[0-9]{3})?|5[1-5][0-9]{14}|6011[0-9]{12}|622((12[6-9]|1[3-9][0-9])|([2-8][0-9][0-9])|(9(([0-1][0-9])|(2[0-5]))))[0-9]{10}|64[4-9][0-9]{13}|65[0-9]{14}|3(?:0[0-5]|[68][0-9])[0-9]{11}|3[47][0-9]{13})*$   "

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
a regex is comprised of 'atoms'; sub units that poses the characters or expectable variation rules for what characters should be expected for a particular relative-character position within the given input string.

### Anchors
Achors are special characters or combinations of characters (and many significant ones ARE special character a'la $ and ^) that tell a regex where in a string it is applying a character-format check.  the start and stop achor for the credit card regex are ^ and $ respectively; 

### Quantifiers
found in the {} brackets throughout the Regex; the quantifiers specify the AMOUNT of a specific character in a given anchors subsection; most are greater than 10 but all of them are less than 16 and 19; the potential number of characters in a credit card number string

### OR Operator
The primary OR opperator for regular expressions "|" is a frequent feature in the credit card regex; likely due to the purely integer nature of a credit card; wheren certain sets of integers are expected and the first 4-6 are almost always a 4-6 character series from a small (compared to the remaining digits) selection of possible serieses (the first four characters of a credit card are usually influenced by the institution issuing the card; however each instituion still has a large set of options here as well; for security purposes there is virtually never ONLY one set of four for any given bank)

### Character Classes
the character classes in the credit card Regex are contained within the angle brackets (ex. "[0-9]") which tells the regex which particular characters; in this case an integer between 0-9 is allowed in that particular section of the expected string.

### Flags
Flags determine the potential match settings for a regular expression; applying potential query-flexers such as "case-insensative" and selecting from multiple potential matches.  As the credit card regex has its potential character possibilities entirely handeled by character classes; AND is built with security in mind; no flags are used in the credit card regex as only proper matches are allowed before any other condition (and purchase) can be achieved.

### Grouping and Capturing
Due to the particular patterns that generate credit card numbers such as different issueing institutions using a small selection of first four numbers; the credit card regex uses a plethora of capturing groups "()"; some nested; with OR operators seperating the different character schemas since there are many imperfections in the exact pattern; however there is still a charcter flow between the potentially 16 or 19 character string that allows certain groupings to expect more frequent patterns of integers.

### Bracket Expressions
Bracket expressions are used primarily to set second round expectations for the character classes; as the character classes ONLY allow integers; the bracket expressions look for certain integers to show up in specific sets of four within the credit card number; reinforcing the expressions expectation of certain integer patterns specifying that this is specifically a credit card recognized by a true banking institution.

### Greedy and Lazy Match
The regex for a credit card uses as much lazy matching as it can which makes sense; as lazy matching conditions; set by the "?" character tellse the mathcing algorythm that it is only looking for a smaller selection of mathcing characters and to reject extranious characters.  This would be expected in a credit card scheme as it is only comprised of integers and would only be exactly 16 or 19 charcters long; and should regect ANY lettering and ANY information that possesses more characters than the set 16 (or rarely 19)

### Boundaries
As boundaries are mostly used by regular expressions to handle the occurance of words and other strings with letter based characters; the regex for a credit card number has no use and therefor does not use any boundaries.

### Back-references
For security purposes; the patterns that one can find in credit card numbers are limited almost entirely to the first 4-6 numbers; the remaining numbers are as random as possible by design.  as this is the case; back-referencing (or using previous information in the expression to influence whats expected later in the string) has no utility in verifying that the integer string is from a credit card.

### Look-ahead and Look-behind
For similar reasons concerning security as the back-reference; the credit card Regex does not have a utility so does not use look-ahead and look-behind assertions; any character that does not match one of the potentials already delineated through other tools should be given no extra information that could lead to searching for a false match.

## Author
Nicholas Holzer
[Link to Profile](https://github.com/NicholasConradHolzer)