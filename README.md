# Tar Heel Shell Development Project
This project is centered around creating a simplistic "Tar Heel" shell interface, aimed at executing basic system programs and changing directories. This venture into system-level programming serves to provide a practical understanding of system-related library functions, instilling a sense of accomplishment as one realizes the ability to build a fundamental element they interact with on a regular basis.

# Tar Heel Shell Development Project

This project entails the construction of a simplified "Tar Heel" shell interface which is aimed at executing basic system operations and changing directories. It presents an engaging venture into system-level programming, offering a practical exploration of system-related library functions. Through this project, you'll gain a sense of achievement as you realize the potential to build a fundamental tool you interact with regularly.

## Project Structure
The project comprises four integral files:
* `Makefile`- houses information for compiling your program with the `make` command. **Modifications not recommended.**
* `shell.h`- includes declarations and specifications for all functions housed in `shell.c`. **Modifications not recommended.**
* `shell.c`- holds function definitions critical for this project, with a primary focus on implementing `find_fullpath` and `execute`.
* `driver.c`- contains the main function which operates in a loop, reading a command and utilizing functions within `shell.c` to validate and manage the command appropriately. **A preliminary review of this file is advised.**

### Shell Basics
Shell commands adopt the format `<command_name> <arg_1> <arg_2> ...` with `<command_name>` representing an executable file and subsequent arguments being parameters passed to the executable. Upon command entry, the shell identifies the absolute path to `<command_name>` and spawns a new process to execute the command. This project delves into the mechanics of how the shell locates and executes commands, with a spotlight on the `PATH` environment variable and the unique built-in commands like `cd` and `exit`.

## System Call Essentials
This project diverges from prior ones as it demands an understanding and manipulation of the system it operates on. It necessitates knowledge on whether a program exists and if so, how to spawn a new process for that program's execution.

Below is a list of potentially useful functions for this project. Familiarize yourself with their syntax and usage by reviewing the documentation for each before proceeding. Detailed information can be garnered using the `man` command from the console or consulting the [`GNU C Library Reference Manual`](https://www.gnu.org/software/libc/manual/html_node/index.html).

* Change directory: `int chdir(const char *path)`
* Fork a process: `pid_t fork(void)`
* Execute binary file: `int execv(const char *file, char *const argv[])`
* Get environment variable: `char getenv(const char *name)`
* Memory allocation: `void *malloc(size t size)`
* Free memory: `void free(void *ptr)`
* File/directory status: `int stat(const char *path, struct stat *buffer)`
* Blocking operation: `pid_t wait(int *status)`

