# Tinitiate UNIX Shell Scripting 
> (c) TINITIATE

## Basic UNIX Shell Scripting

### [Introduction to UNIX](introduction-to-unix.md)
- Overview of UNIX
- What is a shell? Introduction to different types of shells
- Basic shell commands

### [Common UNIX Commands](common-unix-commands.md)
- command: ls
- command: cd
- command: cp
- command: mv
- command: rm, rmdir
- command: touch

### [Getting Started with Shell Scripting](running-a-shellscript.md)
- Creating and running a unix shell script
- Making scripts executable
- Shell script structure (shebang, comments, etc.)

### [Basic Shell Commands and Constructs](shellscript-constructs.md)
- Variables and data types
- Arrays and associative arrays: basics and usage

### [Input and Output](unix-input-output.md)
- Reading user input (`read` command)
- Displaying output (`echo`, `printf`)
- Redirecting output to files and input from files

### [Control Structures](control-structures.md)
- Advanced use of `if-else` and nested `if` statements
- `Case` statements for multi-way branching
- Logical Operators
  - &&: Logical AND
  - ||: Logical OR
  - !: Logical NOT
- Mathematical Operators  
  -lt: Less than (used in numerical comparisons)
  -le: Less than or equal to
  -gt: Greater than
  -ge: Greater than or equal to
  -eq: Equal to
  -ne: Not equal to

### [Loop Control](loop-control.md)
- Advanced loops and loop control (`break`, `continue`)
- Iterating over arrays
- Sequences and patterns in loop statements

### [Arithmetic Operators](arithmetic-operators.md)
- Basic arithmetic operations (`+`, `-`, `*`, `/`, `%`)
- Advanced arithmetic with `expr` and `bc`
- Handling floating-point arithmetic

### [String Operators](string-operators.md)
- String concatenation and manipulation
- Pattern matching and regular expressions with `grep`
- Parameter expansion and substring extraction

### [Function Definition and Usage](function-definition.md)
- Defining and calling functions
- Passing arguments to functions
- Returning values from functions

### [Error Handling in Functions](error-handling.md)
- Handling errors with exit status
- Using `trap` to catch signals
- Debugging functions with `set -x`

### [Advanced I/O Management](file-io.md)
- File System operations
- Here documents and here strings for multi-line input
- Command substitution and pipelines
- Managing file permissions and ownership with `chown`, `chmod`
- File Test Operators
  -e: Test if a file exists
  -f: Test if a file is a regular file
  -d: Test if a file is a directory
  -r: Test if a file is readable
  -w: Test if a file is writable
  -x: Test if a file is executable
  -s: Test if a file is not empty
  -nt: Test if file1 is newer than file2
  -ot: Test if file1 is older than file2
  -ef: Test if two files are the same

### [Process Management](process-management.md)
- Background processes and job control
- Monitor Process `ps`
- Running commands in the background using `&` and `nohup`
- Signals and traps (catching interrupts)
- Managing user permissions with `su` and `sudo`

### [Scripting for Automation Crontab](unix-crontab.md)
- Automating system tasks
- Scheduling scripts using `cron` and `at`

### [Advanced Data Processing with Sed and Awk](sed-aws.md)
- Regular expressions and pattern matching
- Complex text processing scenarios
- Integrating `awk` and `sed` in scripts

## [Special Operators](special-operators.md)
- `$0` The filename of the current script.
- `$n` variables as arguments with which a script was invoked. n is a positive decimal number corresponding to the position of an argument
- `$#` The number of arguments supplied to a script.
- `$*` All the arguments are double quoted. If a script receives two arguments, $* is equivalent to $1 $2.
- `$@` All the arguments are individually double quoted. If a script receives two arguments, $@ is equivalent to $1 $2.
- `$?` The exit status of the last command executed.
- `$$` The process number of the current shell. For shell scripts, this is the process ID under which they are executing.
- `$!` The process number of the last background command.

### [Security and Portability]()
- Security best practices in shell scripting
- Ensuring script portability across different UNIX flavors
- Environment variables and setup
- Secure scripting with `sudo` and environment sanitizations

### [Shell Script Debugging](script-debugging.md)
- Debugging techniques (using `set -x`, `echo` statements)
- Common errors and troubleshooting tips

### [Performance Optimization](performance-optimization.md)
- Profiling and optimizing shell scripts
- Avoiding common pitfalls in script performance

### [Real-World Applications](realworld-applications.md)
- Developing real-world applications using shell scripts
- Case studies of effective script utilization in administration and automation
