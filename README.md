# URL Regex

Regex, or Regular Expressions, are patterns that are set up by computers to provide limitations to certain strings. In this example, I am taking a URL and breaking it down in order to explain how a URL can be pulled from the regular expression below.

## Summary

A URL has a few components to it that are seen across the web. The regex expression is used to identify what characters can be used within a URL, as well as including the essential parts that every URL contains. I will place the expression below and break down and explain what each part means.

URL RegEx
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

<mark>/^</mark>(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?<mark>$/</mark>

The highlighted pieces of the code above mark the anchors, which are what start and end the expression. The first part (/^) begins the expression and comes before the first part, while the last part (/$) states that the expression is finished. All the information contained within these two anchors provides the standards for what is allowed in a URL.

### Quantifiers

/^<mark>(https?:\/\/)?</mark>([\da-z\.-]+)\.([a-z\.]{2,6})<mark>([\/\w \.-]*)*</mark>\<mark>/?</mark>$/

In the first part with the https, there are two quantifiers marked by a "?" symbol. The question marks stand for the pattern matching zero or one time. In this instance, the first part of the url can be written as http or https, or it can be ignored entirely and skip the http(s). Likewise, the question mark at the end of the regex signifies that the forward slash at the end isn't required either, though most of the time it will be shown on a url.

Next, asterisks can be used as a quantifier as well, which is seen at the end of ([\/\w \.-]*)*. This gives the website the ability to follow any pathing that may be required for a certain part of the website. Because it is an asterisk, nothing is required to be after the forward slash.

### Grouping Constructs

/^<mark>(https?:\/\/)</mark>?<mark>([\da-z\.-]+)</mark>\.<mark>([a-z\.]{2,6})</mark><mark>([\/\w \.-]*)</mark>*\/?$/

Grouping constructs provide information within parenthesis pertaining to the given regex. In this case, the URL regex is composed of several components: the https section, the site's name section, the section that follows the dot (such as .com, .net, etc), and the section that follows the overall link. Each section has a certain criteria that it will follow, such as what digits, letters, or symbols are allowed, as well as how many are expected.

### Bracket Expressions

/^(https?:\/\/)?(<mark>[\da-z\.-]</mark>+)\.(<mark>[a-z\.]</mark>{2,6})(<mark>[\/\w \.-]</mark>*)*\/?$/

The brackets give the regex a certain criteria to fulfill. The first bracket, which is the name of the website, only allows lowercase letters, digits, "-" and ".". The second one follows a similar pattern, but without the dashes. Lastly, the final part allows just about any digit or letter, lowercase or uppercase. The \w essentially signifies that it can be a letter a-z or A-Z, as well as 0-9 and an underscore.


### Character Classes

/^(https?:\/\/)?([<mark>\d</mark>a-z\.-]+)\.([a-z\.]{2,6})([\/<mark>\w</mark> \.-]*)*\/?$/

The two character classes shown above (\d and \w) allow a certain type of characters to be displayed. \d, for instance, allows numbers between 0-9 to be used, so in that bracket, lowercase letters AND numbers can be input. As for the \w, any number or letter, be it upper or lowercase, can be input. Likewise, \w allows for underscores.

### Character Escapes

/^(https?:<mark>\/\/</mark>)?([\da-z\.-]+)<mark>\.</mark>([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

In the above highlights, the "\/\/" ensures that the computer knows that a double forward slash IS required after the https section. The back slash signifies that it wants the literal forward slash to be inserted here. Likewise, the \. requires the dot to follow the site name section, as one can see by looking at any URL where a .com or other variant follows the url's site name.

## Author

Allyson Pacheco
https://github.com/alycioe
