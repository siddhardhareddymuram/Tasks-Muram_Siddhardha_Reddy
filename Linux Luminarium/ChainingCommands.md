## Module 11: Chaining Commands

* ### Chaining with Semicolons

![image](https://github.com/user-attachments/assets/53139794-00e0-404c-be53-ba02266a27f9)

The semicolon `;` allows multiple commands to be written on the same line. The shell executes the command before the semicolon first and then moves on to the next command, regardless of whether the previous command succeeds or fails.

* ### Your First Shell Script

![image](https://github.com/user-attachments/assets/f7bab228-d202-496e-96a7-f79270fe5ded)

This challenge introduces the basics of creating and running a shell script. A shell script is a file containing a sequence of commands that can be executed together. I referred to a tutorial to understand the basic structure and syntax required to create one.

* ### Redirecting Script Output

![image](https://github.com/user-attachments/assets/affff039-6e40-46cc-9533-99c8d56c9684)

The script can be executed using `bash`, and its output can then be passed directly to another program using a pipe. Here, the output of the script is piped into `/challenge/solve` so that it can process the generated data.

* ### Executable Shell Scripts

![image](https://github.com/user-attachments/assets/d226cb78-965a-4ba0-ac43-abad070dbdfe)

A shell script can be made executable by modifying its file permissions. Once execute permission is enabled, the script can be run directly instead of explicitly invoking it with `bash`.
