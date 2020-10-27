# <center>Cheat sheet for bash</center>
- Most of this information may be found with `man bash`.

## REDIRECTIONS
### Redirecting input
* generally is `[n] < word`. 
* Example 
```console
$cat < test.txt
Just a simple file
Nothing unusual.
```
### Redirecting output
* `[n] > word`
## Appending redirected output
* `[n] >> word`
## FIND COMMAND

### `-type` parameter
 * `f` search all files 
 * `d` search all directories
 
### `-name` parameter (`-iname` for case-insensetive)
* Takes a glob as parameter (`"app"`, `"*.c"`, `"*.C"`)

### `-path` parameter (`-ipath` for case-insensitive)
* Works as `-name`, except doesn't only apply the pattern to filenames.

## IF STATEMENTS
* General rule for `if` statement
```bash
if [CONDITION]
then
  command1
  command2
  ...
  commandn
fi
```
* General rule for `if..else` statement
```bash
if [CONDITION]
then
  ...
else
  ...
fi
```
* General rule for `if..elif..else` statement
```bash
if [CONDITION1]
then
  ...
elif [CONDITION2]
then
  ... 
else
  ...
fi
```
* Nested `if` statements
```bash
if [CONDITION]
then
  if [CONDITION]
  then
    command1
    command2
    ...
    commandn
  fi
  command1
  command2
  ...
  commandn
fi
```
## CONDITIONAL EXPRESSIONS
> :warning: You should pay attetntion to spaces between lexemas. For example `[-a $FILE]` won't work.  

C.E. are widely used in if statements, for and while loops, where ommited by `[]` and `[[]]`
* Single-file conditional operators
  * `[ -a file ]` - if file exists.
  * `[ -b file ]` - if file exists and is a block special file.
  * `[ -c file ]` - if file exists and is a character special file.
  * `[ -d file ]` - if file exists and is a directory.
  * `[ -e file ]` - if file exists.
  * `[ -h file ]` - if file exists and is a symbolic link.
  * `[ -r file ]` - if file exists and readable.
  * `[ -s file ]` - if file exists and it's size greater than zero.
  * `[ -w file ]` - if file exists and it is writable.
  * `[ -x file ]` - if file exists and it is executable.
  
* Multiple-files conditional operators
  * `[ file1 -nt file2 ]` - file1 Newer Then file2.
  * `[ file1 -ot file2 ]` - older than.
  
* Single-string conditional operators
  * `[ -z string ]` - if string is zero.
  * `[ -n string ]` - if string is non-zero.
  
* Multiple-string conditional operators
  * `[ string1 == string2 ]` - if strings are equal.
  * `[ string1 != string2 ]` - if strings are not equal.
  * `[ string1 < string2 ]` - if string1 sorts before string2 lexicographically.
  * `[ string1 > string2 ]` - if string1 sorts after string2 lexicographically.
  
* Arithmetic conditional operators
  * `[ arg1 -eq arg2 ]` - arg1 is equal to arg2.
  * `[ arg1 -ne arg2 ]` - arg1 is not equal to arg2.
  * `[ arg1 -lt arg2 ]` - arg1 is less then arg2.
  * `[ arg1 -le arg2 ]` - arg1 is less or equal to arg2.
  * `[ arg1 -gt arg2 ]` - arg1 is greater then arg2.
  * `[ arg1 -ge arg2 ]` - arg1 is greater or equal to arg2.
    
## FOR LOOPS
* General rule
```bash
for VARIABLE in 1 2 3 4 5 .. N
do
	command1
	command2
 ...
	commandn
done
```
* Using ranges. You also can use seq command(`seq start end step`)
```bash
# Simple range with step = 1 
for i in {1..5}
do
   printf "this is %d loop\n" $i
done
# With manually defined step
for i in {0..10..2} #From 0 to 12 with step 2.
do 
     printf "this is %d loop\n" $i 
done
```
* Ranges, but more programming style.
```bash
for (( c=1; c<=5; c++ ))
do  
   printf "this is %d loop\n" $i
done
# Infinite loop
for (( ; ; ))
...
```
* Examples
Iterate over files in c
```bash
for f in $(ls -p | grep -v /) # iterate over files ONLY
do
...
done 
```
## WHILE LOOPS
* General rule
```bash
while [CONDITION]
do
	command1
	command2
 ...
	commandn
done
```
## PARAMETER EXPANSION
* `${parameter}` - substitute with parameter value. 
* `${parameter:-word}` - Use Default Value. So if `parameter` is unset or null will be replaced with `word `in THIS statement.
* `${parameter:=word}` - Assign Default Value. The `word` will be assigned to `parameter` globally. 
* `${parameter:offset[:length]}` - Returns offseted value with specific length (if defined).
* `${}`
## SUBSTITUTIONS
* Rule for commands: `$(command)` or `command`(with backticks)
