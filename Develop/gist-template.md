# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.
//explain that i am going to explain what regex but also define this string

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Escapes](#character-escapes)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components
1. The string is 3-16 characters long.
2. The string can contain:
    -any lower case a-z
    -any number 0-9
    -an underscore or hyphen

    example: <"abc_123">


### Anchors
Anchors are the characters ^ or $.
-With the ^ anchor, it shows that a string with characters will follow. This could happen in two different contexts.
    -With an exact string match
    -a grouping of possible matches
-With the $ anchor, it will end the string. It follows the same two contexts as ^

example: <"^abc_123$">

### Quantifiers
-The last requirement of the regex is the length of the string. A quantifier will set the limits on the string that is used in regex matches. Quantifiers constantly look for the limits that can be used to find a match. 
    They look for patterns like:
    *- matches zero or more times
Example: 'd*o*g*' = ddooo or doooogg
    +- matches one or times
    ?- matches zero or one time
    {}- has 3 different limits
        1. {n}- which matches the pattern n times exactly
        2.{n, } which matches the pattern n times exactly
        3.{n, x} which matches from a minimun n to a maximum of x


### OR Operator
A bracket expression does not need to meet all of requirements to make or look for a pattern. You can include one or two in the pattern.
Outside of the bracket you can add the same logic. One or two special characters, within a grouping contruct or two different constructors.
### Character Escapes 
The \ (backlash) escapes character instead of looking at it literally. The way this translates is that if you include the \ before the ({), it changes the curly bracket to look for a curly brack instead of looking for a quantifier. The back slash is common looking for strings with characters that are the same within the pattern.

All special characters including (\) lose their special significance inside the bracket expression. 

\3= looks for "3" instead of looking for 3 matches.
[\3]= loses all significance beyond whatever the string matches 
 
### Character Classes
A character class is defined in an input string when looking for a match. 
    Character classes:
        -Bracket expressions (as described below)
        -positive and negative character groups
        -. matches any character except newline character
        -\d matches any arabic numeral digit. Very similiar to bracket expresson [0-9] 
        -\w matches of alphanumeric from latin alphabet including _ -This class is the same to the bracket expression [A-Za-z0-9_]
        -\s matches a single whitespace character. It can include tabs and line breaks.  
        Lastly, the last three classes change be changed to do inverse search. This is done by capitalizing the letter character. 


### Flags
A regex have to be wrapped in slash characters, with some exceptions. There are six total things called Flags that you need to be aware of. The three below are the most likely ones that you are run into.
1. g- global search, testing targets all possible matches in a string
2. i case-insensitive search: case should be ignore in any search. 
3. m multi-line search: multi-line input string which would treated as multiple lines.

### Grouping and Capturing
Grouping- any part of the regular expression together.

Capturing groups treat multiple character as single unit. To capture a group by putting parentheses. This groups can be saved for later search, see backreferences.

### Bracket Expressions
-Anything that is inside the square brackets. This can stand for the characters that are being matched. 
-Another name for bracket expressions is positive character group.
-Often the hyphen is used between alphnumeric character, like abc or 123
    I.E. - [a-c] = [abc]
    I.E. - [1-3] = [123]
 Special character are either the underscore _ or the hyphen -. Special characters can be any non alphanumeric characters. There is a hyphen that is used in alphanumeric but it is used different and you must noted the difference. 
 When a combination of the above is put together, it will match any string This is combination of lowercase letters a-z, and any number 0-9, and the special characters.
 NOTE: these strings do not include any upper case letters.      
### Greedy and Lazy Match

If you add a ? to the quantifiers, it makes it lazy which makes it match only a few occurences as possible.          

Quantifiers are greedy, as they will find any patterns that they find. 
 
### Boundaries
Boundary markers like ^ or $ allow the search to focused on the pattern at the beginning and end of the line/ string. If you would like to have a literal match, you will have to escape using a backlash. (see character escape above).

### Back-references
if you use regular expressions to match against string pattens, it may happen where you would like to match the same piece of text two or more times. 
A backreference within in a regular expression will use a previously matched pattern and will look for the same pattern or text again. 
    -numbered backreferences
        has already matched a string or text in a group. THe search needs a backlash \ at the beginning and the number of the group to match again.
    -named backreferences
        In order to not have to search each group by individual character, once a group has been found, you then can name it. Naming the gorup, allows you search using that name. If the name is the same more than once, the search will send back the most recent one 
### Look-ahead and Look-behind
Lookaheads and lookbehinds are often called lookarounds. These tyes of capture groups traverse text until a certain patterns happens.
Traversing is a process where each element of the data structure is access. Lookarounds traverse around at the beginning of the line. Lookbehinds traverses at the end of the line. 
## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
