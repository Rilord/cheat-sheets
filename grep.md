# GREP


### Function call

```grep
grep [options] [regexp] [filename]
```

### Meta characters
* `^` - beggining of the line.
* `$` - end of line.
* `.` - any character.
* `*` - zero or more instances of this character (iteration).
* `[]` - one character containing in the set.
* `[^]` - one character NOT containing in the set.
* `\<` - beggining of the word.
* `\>` - end of the word.
* `{character}\{m[,n]\}` - iteration of character m or optionally between m and n times.
* `\w` - word character.
* `\W` - not word character.
* `\b` - word boundary.

The listed meta characters are part of basic set regex syntax and here is the advanced set:

* `+` - one or more preceeding characters.
* `?` - zero or more preceeding characters.
* `x|y|z` - matches either x or y or z.
* `()` - group characters.


### Basic regexes
* other

### Examples of function call
* 



### Useful sources
* https://docs.oracle.com/cd/E19253-01/806-7612/filesearch-4/index.html
