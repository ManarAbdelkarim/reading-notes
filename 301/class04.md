# Read: 04 - Responsive Web Design and Regular Expressions

## CSS Grid
-----------
The CSS Grid Layout Module offers a grid-based layout system, with rows and columns, making it easier to design web pages without having to use floats and positioning.


CSS Grid Layout is the most powerful layout system available in CSS. It is a 2-dimensional system, meaning it can handle both columns and rows, unlike flexbox which is largely a 1-dimensional system.

### Properties for the Parent (Grid Container)

### **display**

Defines the element as a grid container and establishes a new grid formatting context for its contents.

Values:
- grid – generates a block-level grid
- inline-grid – generates an inline-level grid

- grid-template-columns
- grid-template-rows

Defines the columns and rows of the grid with a space-separated list of values. The values represent the track size, and the space between them represents the grid line.

Values:
- <track-size> – can be a length, a percentage, or a fraction of the free space in the grid (using the fr unit)
- <line-name> – an arbitrary name of your choosing


### Get Started With Grid :
To get started you have to:
-  define a container element as a grid with display: grid
- set the column and row sizes with grid-template-columns and grid-template-rows
- place its child elements into the grid with grid-column and grid-row. Similarly to flexbox

the source order of the grid items doesn’t matter. Your CSS can place them in any order, which makes it super easy to rearrange your grid with media queries.



## Bookmark/Skim

### RegExr
 - RegExr is an online tool to learn, build, & test Regular Expressions (RegEx / RegExp).

1 | Character classes
------------ | -------------
`.` | any character except newline
`\w\d\s` | word, digit, whitespace
`\W\D\S` | not word, digit, whitespace
`[abc]` | any of a, b, or c
`[^abc]` | not a, b, or c
`[a-g]` | character between a & g

2 | Anchors
------------ | -------------
`^abc$` | start / end of the string
`\b\B` | word, not-word boundary

3 | Escaped characters:
`\.\*\\` | escaped special characters
`\t\n\r` | tab, linefeed, carriage return

4 | Groups & Lookaround:
------------ | -------------
`(abc)` | capture group
`\1` |backreference to group #1
`(?:abc)` | non-capturing group
`(?=abc)` | positive lookahead
`(?!abc)` | negative lookahead

5 | Quantifiers & Alternation:
------------ | -------------
`a*a+a?` | 0 or more, 1 or more, 0 or 1
`a{5}a{2,}` | exactly five, two or more
`a{1,3}` | between one & three
`a+?a{2,}?` | match as few as possible
`ab|cd` | match ab or cd
