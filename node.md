
# Node Cheat sheets

### Command line arguments
* `-v, --version` shows version.
Example: 
```bash
node -v 
v14.13.0
```
* `-c, --check` syntax check the script without further execution.
* `-e, --eval "script"` evaluate the command line argument followed by this parameter. 
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
* `-p, --print "script"` simmilar to `-e`, but with result print.
* `--prof` generate V8 profiler output to file `*.log`.
Example: 
```bash
$ cat index.js
var a = new Int32Array([4945, -63456]);
console.log(a);
$ node --prof index.js
$ ll 
isolate-a-b-v8.log
```

* `--no-warnings` silence all warnings.

* `--heap-prof` generates heap profile and saves to file `*.heap` before exit.

