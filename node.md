
# Node Cheat sheets

### Command line arguments
* `-v, --version` shows version 
* `-c, --check` syntax check the script without further execution 
* `-e, --eval` evaluate the command line argument followed by this parameter. 
Example: 
```bash
$ node -e 'var x = 6; console.log(x);'
6
```
* `-i, --interactive` open a REPL instance. .exit stands for exit.
Example: 
```bash
$ node -i
Welcome to Node.js v14.13.0.
Type ".help" for more information.
> var x = 6;
undefined
> x
6
```
* `-p, --print `
