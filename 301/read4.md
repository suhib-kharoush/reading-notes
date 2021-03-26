# Regex:
- Basic topics:
- ^The: matches any string that starts with The.
- ^The end$: exact string match.
- roar matches any string that has the text roar in it.

- Quantifiers -*+? and {}:
- abc*: matches a string that has ab followed by zero or more c -
- abc+: matches a string that has ab followed by one or more c
- abc?: matches a string that has ab followed by zero or one c
- abc{2} matches a string that has ab followed by 2 c
- abc{2, }: matches a string that has ab followed by 2 or more c
- abc{2,5}: matches a string that has ab followed by 2 up to 5 c
- a(bc)* matches a string that has a followed by zero or more copies of the sequence bc
a(bc){2,5}: matches a string that has followed by 2 up to 5 copies of the sequence bc

OR operator -|or[]:
- a(b|c): matches a string that has a followed by b or c and capture b or c
a[bc]: the same as before but without capture

- Character classes -\d\w\s and .:
- \d matches a single character that is a digit 
- \w: matches a word character 
- \s: matches a whitespace character
- .: matches any character

- Flags:
- g (global) does not return after the first match
- m (muti-line): when enabled ^ and $ will match the start and end of a line instead of whole string
- i (insensitive): makes the whole expression case- insensitive

- Grid properties:

- grid: generates a block-level grid
- inline-grid: generates an inline-level grid

- grid-column-start
- grid-column-end
- grid-row-start
- grid-row-end

- Determines a grid item’s location within the grid by referring to specific grid lines. grid-column-start/grid-row-start is the line where the item begins, and grid-column-end/grid-row-end is the line where the item ends.


