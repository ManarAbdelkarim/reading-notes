# Automation

![](https://www.openaccessgovernment.org/wp-content/uploads/2021/03/dreamstime_s_126377515.jpg)

What Does Automation Mean?
Automation is the creation and application of technologies to produce and deliver goods and services with minimal human intervention. The implementation of automation technologies, techniques and processes improve the efficiency, reliability, and/or speed of many tasks that were previously performed by humans.
## Regular expression

![](https://miro.medium.com/max/1400/1*oaFozQztiv9WMMcwX9m9HQ.jpeg)

Regular Expressions, often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text `(string)` or not. 

**`re`** : Python library that supports regular expressions


### Basic Patterns: Ordinary Characters:
Ordinary characters are the simplest regular expressions. They match themselves exactly and do not have a special meaning in their regular expression syntax.
Examples are 'A', 'Manar' , '5'.
r"Manar"


### Wild Card Characters: Special Characters:
Special characters are characters that do not match themselves as seen but have a special meaning when used in a regular expression.

**`.`** - A period. Matches any single character except the newline character.

**`^`** - A caret. Matches the start of the string.

**`$`** - Matches the end of string.

**`[abc]`** - Matches a or b or c.

**`[a-zA-Z0-9]`** - Matches any letter from (a to z) or (A to Z) or (0 to 9).

**`[^]`** all the characters that are not in the set will be matched.

**`\ - Backslash.`** : 
- If the character following the backslash is a recognized escape character, then the special meaning of the term is taken 

- Else if the character following the \ is not a recognized escape character, then the \ is treated like any other character and passed through .

- \ can be used in front of all the metacharacters to remove their special meaning

**`\w`** : Lowercase 'w'. Matches any single letter, digit, or underscore.

**`\W`** : Uppercase 'W'. Matches any character not part of \w (lowercase w).

**`\s`** - Lowercase 's'. Matches a single whitespace character like: space, newline, tab, return.

**`\S`** - Uppercase 'S'. Matches any character not part of \s (lowercase s).

**`\d`** - Lowercase d. Matches decimal digit 0-9.

**`\D`** - Uppercase d. Matches any character that is not a 
decimal digit.

**`\t`** - Lowercase t. Matches tab.

**`\n `**- Lowercase n. Matches newline.

**`\r `**- Lowercase r. Matches return.

**`\A`** - Uppercase a. Matches only at the start of the string. 
Works across multiple lines as well.

**`\Z`** - Uppercase z. Matches only at the end of the string.

**`\b`** - Lowercase b. Matches only the beginning or end of the word.

**`+`** - Checks if the preceding character appears one or more times starting from that position.

**`*`** - Checks if the preceding character appears zero or more times starting from that position.

**`?`** - Checks if the preceding character appears exactly zero or one time starting from that position.

**`{x}`** - Repeat exactly x number of times.

**`{x,}`** - Repeat at least x times or more.

**`{x, y}`** - Repeat at least x times but no more than y times.

**`*?`** that matches as little text as possible.Adding `?` after the qualifier makes it perform the match in a non-greedy or minimal fashion; That is, as few characters as possible will be matched


#### **r** :
 raw string literal. It changes how the string literal is interpreted. Such literals are stored as they appear
#### **match()** :
 function returns a match object if the text matches the pattern. Otherwise, it returns None

 The match() function checks for a match `only at the beginning of the string (by default)`
#### **compile()**:
`compile(pattern, flags=0)`

with `compile()`, you can computer a regular expression pattern into a regular expression object. When you need to use an expression several times in a single program, using compile() to save the resulting regular expression object for reuse is more efficient than saving it as a string.

#### **search()** :
`search(pattern, string, flags=0)`

 search function, you scan through the given string/sequence, looking for the first location where the regular expression produces a match.
 the search() function checks for a match `anywhere in the string`.
 #### **group** : 
 The group function returns the string matched by the re.
  Named groups will make your code more readable. The syntax for creating named group is: (?P<name\>...)
#### **findall()**:
`findall(pattern, string, flags=0)`

Finds all the possible matches in the entire sequence and returns them as a list of strings. Each returned string represents one match.

### **finditer()**

`(string, [position, end_position])`

Similar to findall() - it finds all the possible matches in the entire sequence but returns regex match objects as an iterator.

#### **sub()**
`sub(pattern, repl, string, count=0, flags=0)`

sub() is the substitute function. It returns the string obtained by replacing or substituting the leftmost non-overlapping occurrences of pattern in string by the replacement repl. If the pattern is not found, then the string is returned unchanged.

#### **subn()**
The subn() is similar to sub(). However, it returns a tuple containing the new string value and the number of replacements that were performed in the statement.

#### **split()**
`split(string, [maxsplit = 0])`

This splits the strings wherever the pattern matches and returns a list. If the optional argument maxsplit is nonzero, then the maximum 'maxsplit' number of splits are performed.


`start()` - Returns the starting index of the match.

`end()` - Returns the index where the match ends.

`span()` - Return a tuple containing the (start, end) positions of the match.

###  compilation flags:

An expression's behavior can be modified by specifying a flag value. You can add flags as an extra argument to the different functions that you have seen in this tutorial. Some of `the more useful ones are:`

- `IGNORECASE (I)` - Allows case-insensitive matches.
- `DOTALL (S)` - Allows . to match any character, including newline.
- `MULTILINE (M)` - Allows start of `string (^)` and end of
`string ($)` anchor to match newlines as well.
- `VERBOSE (X)` - Allows you to write whitespace and comments within a regular expression to make it more readable.