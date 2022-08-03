## What is a shell
THe shell is a program that receive commands from user, from keybord to send them to the explotation system in charge of executing them.

"Shell" signifies interface system. Shell designates the lowest layer of all the interfaces systems.

What's the use of a script in shell?
On most Linux systems, a program is called bash (signifies Bourne again Shell) act as shell program. All shell can execute commands located in files. Each file containing commands intended for shell is called a script. A script looks like a file text executable by the machine. but need to be interpreted by the terminal emulator. It's objective is to launch and coordinates the execution of programs without passing by the graphic interface.

## Exercices
Write a UNIX command line interpreter

The shell should: • Display a prompt and wait for the user to type a command. A command line always ends with a new line. • The prompt is displayed again each time a command has been executed. • The command lines are simple, no semicolons, no pipes, no redirections or any other advanced features. • The command lines are made only of one word. No arguments will be passed to programs. • If an executable cannot be found, print an error message and display the prompt again. • Handle errors. • You have to handle the “end of file” `condition (Ctrl+D)`.

## Simple Shell

- We created a basic version of the Unix shell from scratch. A program that takes commands from the keyboard and gives them to the operating system to perform. The shell can perform commands such as listing files in current working directory by typing `ls`, `exit`, among others. It works in both interactive and non-interactive mode.

- The following are the allowed functions and system calls.
- `access`, `chdir`, `close`, `closedir`, `execve`, `exit`, `_exit`, `fflush`, `fork`,`free`, `getcwd`, `getline`, `getpid`, `isatty`, `kill`, `malloc`, `open`, `opendir`, `perror`, `read`, `readdir`, `signal`, `stat`, `lstat`, `fstat`, `strtok`, `wait`, `waitpid`, `wait3`, `wait4`, `write`

## File Descriptions

- `AUTHORS`: Has the names of this project's contributors.
- ```execute```: Contains the function that executes shell commands.
- `_strings.c`, `_strings2.c`, `_strings3.c`: Contains functions that are used to manipultate and get data about strings like finding string length and splitting a string.
- `built-in.c`: Includes functions to perform built-in shell command operations like `exit`.
- `main.h`: Holds all function prototypes and headers.
- `main.c`: The shell's entry point i.e contains the main method.
- `man_1_simple_shell`: A manual for the shell.
- `prompt.c`: Prints the shell's title to indicate the shell is ready to receive input.
- `readline`: Responsible for picking commands typed into the shell.
- `handle_path.c`: Contains functions used to handle cases when a command is entered into the shell instead of the path to the executable file. For example when a use types `ls` instead of `\bin\ls`;

## How to use the shell

- Install

```
(your_terminal)$ git clone <this repository>
(your_terminal)$ cd simple_shell
```
- Compile

```
gcc -Wall -Werror -Wextra -pedantic *.c -o hsh
```

- Usage: non-interactive mode

```
echo "/bin/ls" | ./hsh
```

- Usage: interactive mode

```
(your_terminal)$ ./hsh
```

## Example

```
#cisfun$ /bin/ls -l
total 68
-rw-rw-r-- 1 vagrant vagrant   168 Aug 3 13:40 AUTHORS
-rw-rw-r-- 1 vagrant vagrant  1761 Aug 3  README.md
-rw-rw-r-- 1 vagrant vagrant   887 Aug   _execute.c

#cisfun$ exit 100
(your_terminal)$
```

## Authors
1. [francis gichuhi](https://github.com/frank-gich)
2. [Gilbert Chukwuemezie](https://github.com/)