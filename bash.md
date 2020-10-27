# <center>Cheat sheet for bash</center>


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

## FOR loops
* General usage
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
## WHILE loops
