# <center>Cheat sheet for bash</center>
- Most of this information may be found with `man bash`.

## Redirections
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
## Find command

### `-type` parameter
 * `f` search all files 
 * `d` search all directories
 
### `-name` parameter (`-iname` for case-insensetive)
* Takes a glob as parameter (`"app"`, `"*.c"`, `"*.C"`)

### `-path` parameter (`-ipath` for case-insensitive)
* Works as `-name`, except doesn't only apply the pattern to filenames.

### Examples


## IF statements
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
## Test condifions and operators
* General rule
```bash
```
* Using in if statements
## FOR loops
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
## WHILE loops
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
## Parameter expansion
* `${parameter}` - substitute with parameter value. 
* `${parameter:-word}` - Use Default Value. So if `parameter` is unset or null will be replaced with `word `in THIS statement.
* `${parameter:=word}` - Assign Default Value. The `word` will be assigned to `parameter` globally. 
* `${parameter:offset[:length]}` - Returns offseted value with specific length (if defined).
* `${}`
## Substitions (commands, arithmetics and processes)
### General rule: `$(command)` or ``command``
