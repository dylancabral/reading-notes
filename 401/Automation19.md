# Automation

Automation is is important to what we are learning about because it allows you to save time and code actions into functions and methods allowing things to be done behind the scenes and allow to speed up the actions of things

## Python Regular Expressions Tutorial

  regex is used at the server side to validate the format of email addresses or passwords during registration, used for parsing text data files to find, replace, or delete certain string, etc. They help in manipulating textual data, which is often a prerequisite for data science projects involving text mining.

  regular expression are supported by 
  ```python
  import re
  ```

  Special characters are characters that are reserved metacharacters that denote something else and not what they look like.

  The **match()** function returns a match object if the text matches the pattern. Otherwise, it returns None

  **search()** can through the given string/sequence, looking for the first location where the regular expression produces a match.

  **group()**returns the string matched by the re.

  ### Special Characters

  - . - A period. Matches any single character except the newline character.
  - ^ - A caret. Matches the start of the string.
  - $ - Matches the end of string.
  - [abc] - Matches a or b or c. 
  - [a-zA-Z0-9] - Matches any letter from (a to z) or (A to Z) or (0 to 9).
  - characters that are not within a range can be matched by complementing the set. If the first character of the set is ^, all the characters that are not in the set will be matched.

  - \ - Backslash.

    - If the character following the backslash is a recognized escape character, then the special meaning of the term is taken (Scenario 1)
    - Else if the character following the \ is not a recognized escape character, then the \ is treated like any other character and passed through (Scenario 2).
    - \ can be used in front of all the metacharacters to remove their special meaning 
  - \w - Lowercase 'w'. Matches any single letter, digit, or underscore.
  - \W - Uppercase 'W'. Matches any character not part of \w (lowercase w).
  - \s - Lowercase 's'. Matches a single whitespace character like: space, newline, tab, return.
  - \S - Uppercase 'S'. Matches any character not part of \s (lowercase s).
  - \d - Lowercase d. Matches decimal digit 0-9.
  - \D - Uppercase d. Matches any character that is not a decimal digit.
  -  +  is used for repetition.
  - \t - Lowercase t. Matches tab.
  - \n - Lowercase n. Matches newline.
  - \r - Lowercase r. Matches return.
  - \A - Uppercase a. Matches only at the start of the string. Works across multiple lines as well.
  - \Z - Uppercase z. Matches only at the end of the string.
  - ^ and \A are effectively the same, and so are $ and \Z. Except when dealing with MULTILINE mode. 
  - \b - Lowercase b. Matches only the beginning or end of the word.

  ## Repetitions
  - ` + - `Checks if the preceding character appears one or more times starting from that position.
  - `* - `Checks if the preceding character appears zero or more times starting from that position.
  - ? - Checks if the preceding character appears exactly zero or one time starting from that position.
  - {x} - Repeat exactly x number of times.
  - {x,} - Repeat at least x times or more.
  - {x, y} - Repeat at least x times but no more than y times.
  - The + and * qualifiers are said to be greedy

  ### Grouping in RegEx

  parts of a regular expression pattern bounded by parenthesis () are called groups. The parenthesis does not change what the expression matches, but rather forms groups within the matched sequence

  The plain match.group() without any argument is still the whole matched text as usual.

  > Imagine you were validating email addresses and wanted to check the user name and host. This is when you would want to create separate groups within your matched text.

  - <> brackets
    - will let you create named groups. Named groups will make your code more readable. The syntax for creating named group is: (?P<name>...). Replace the name part with the name you want to give to your group. The ... represent the rest of the matching syntax.

    - you can always access the named groups using numbers instead of the name. But as the number of groups increases, it gets harder to handle them using numbers alone. So, always make it a habit to use named groups instead.

  ### functions in RE

  - compile()

    * you can computer a regular expression pattern into a regular expression object. When you need to use an expression several times in a single program, using compile() to save the resulting regular expression object for reuse is more efficient than saving it as a string. This is because the compiled versions of the most recent patterns passed to compile() and the module-level matching functions are cached.

  - search()

    * With this function, you scan through the given string/sequence, looking for the first location where the regular expression produces a match. It returns a corresponding match object if found, else returns None if no position in the string matches the pattern. Note that None is different from finding a zero-length match at some point in the string.

  - match()
    * Returns a corresponding match object if zero or more characters at the beginning of string match the pattern. Else it returns None, if the string does not match the given pattern.

  The match() function checks for a match only at the beginning of the string (by default), whereas the search() function checks for a match anywhere in the string.

  - findall()
    * Finds all the possible matches in the entire sequence and returns them as a list of strings. Each returned string represents one match.

  - finditer()
    * Similar to findall() - it finds all the possible matches in the entire sequence but returns regex match objects as an iterator.

  - sub() 
    * the substitute function. It returns the string obtained by replacing or substituting the leftmost non-overlapping occurrences of pattern in string by the replacement repl. If the pattern is not found, then the string is returned unchanged.

  - ubn()
    * it returns a tuple containing the new string value and the number of replacements that were performed in the statement.

  - split(string, [maxsplit = 0])
    * splits the strings wherever the pattern matches and returns a list. If the optional argument maxsplit is nonzero, then the maximum 'maxsplit' number of splits are performed.

  - start() - Returns the starting index of the match.
  - end() - Returns the index where the match ends.
  - span() - Return a tuple containing the (start, end) positions of the match.

  ### complitation Flags

  - IGNORECASE (I) - Allows case-insensitive matches.
  - DOTALL (S) - Allows . to match any character, including newline.
  - MULTILINE (M) - Allows start of string (^) and end of string ($) anchor to match newlines as well.
  - VERBOSE (X) - Allows you to write whitespace and comments within a regular expression to make it more readable.

## Shutil

  ### copying
  * copyfile() copies the contents of the source to the destination and raises IOError if it does not have permission to write to the destination file.
    * Because the function opens the input file for reading, regardless of its type, special files (such as Unix device nodes) cannot be copied as new special files with copyfile().
    * The implementation of copyfile() uses the lower-level function copyfileobj(). While the arguments to copyfile() are filenames, the arguments to copyfileobj() are open file handles. The optional third argument is a buffer length to use for reading in blocks.
    * default behavior is to read using large blocks. Use -1 to read all of the input at one time or another positive integer to set a specific block size. This example uses several different block sizes to show the effect.

  * copy() function interprets the output name like the Unix command line tool cp. If the named destination refers to a directory instead of a file, a new file is created in the directory using the base name of the source.
    * permissions of the file are copied along with the contents.
    * copy2() works like copy(), but includes the access and modification times in the metadata copied to the new file.
      * The new file has all of the same characteristics as the old version.

  * copymode() To copy the permissions from one file to another
    * copystat() To copy the permissions from one file to another
      * Only the permissions and dates associated with the file are duplicated with copystat()

  ### Directory Trees
  * copytree() To copy a directory from one place to another, recurses through the source directory tree, copying files to the destination. The destination directory must not exist in advance

## Automation Ideas

  you can use automation to traverse through files, send emails update you about your favorite youtuber posting a new video, you can have it iterate how you store documents like using regex to understand the type of file and import it to a predetermined location, automation is very very cool, i have watched videos where people have smartified their offices with scripts, I hope i have the time and money yto do that in the future

## Automationg your browser and desktop apps
  optional **AM TIRED**

## Things I want to Know more about 

  I cant wait until regex is just built into my brain this is some dense stuff 

## Resources

[Python Regular Expressions Tutorial](https://www.datacamp.com/community/tutorials/python-regular-expression-tutorial)

[shutil](https://pymotw.com/3/shutil/)

[Automation Ideas](https://www.youtube.com/watch?v=qbW6FRbaSl0&t=69s)

[Automating Your Browser and Desktop Apps](https://www.youtube.com/watch?v=dZLyfbSQPXI)

[Watchdog](https://pythonhosted.org/watchdog/)
