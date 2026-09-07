## Module 8: Processes and Jobs

* ### Listing Processes

![image](https://github.com/user-attachments/assets/ab20cbc0-4995-4308-b143-d81de520ae0a)

The `ps -ef` and `ps aux` commands are used to view processes currently running on the system. By examining the process list, we can identify the relevant challenge process and determine which process needs to be handled to obtain the flag.

* ### Killing Processes

![image](https://github.com/user-attachments/assets/46388078-e795-4d4a-a1c5-f685695f6f68)

The `kill` command is used to terminate a running process by specifying its process ID (PID). In this challenge, we identified the `/challenge/dont_run` process and terminated it before executing `/challenge/run`.

* ### Interrupting Processes

![image](https://github.com/user-attachments/assets/c2bcd9c1-c749-4a60-b46d-5900184fee95)

The `Ctrl-C` keyboard shortcut sends an interrupt signal to the currently running process. It is commonly used to stop a command or exit a program that is running in the terminal.

* ### Suspending Processes

![image](https://github.com/user-attachments/assets/4cc9e797-a9e6-41c5-ba3f-86d75e0d46c9)

The `Ctrl-Z` shortcut temporarily suspends the currently running process. Instead of terminating it, the process is paused and can be resumed later.

* ### Resuming Processes

![image](https://github.com/user-attachments/assets/064402a6-288c-4551-9ab1-86d4a25c5eed)

The `fg` command brings a suspended or background process back into the foreground. This allows the process to continue running while the terminal waits for it to finish.

* ### Backgrounding Processes

![image](https://github.com/user-attachments/assets/ba598124-fa9e-4717-ab41-913403382414)

![image](https://github.com/user-attachments/assets/b42f802c-9cd1-4567-8bb6-ece3faa948d9)

The `bg` command resumes a suspended process but keeps it running in the background. This allows us to continue using the terminal while the process executes.

* ### Foregrounding Processes

![image](https://github.com/user-attachments/assets/259783ef-50d4-43f0-a0db-8c0d8c877310)

A background process can be brought back to the foreground using `fg`. In this challenge, we go through multiple steps to identify the required job and move it from the background to the foreground.

* ### Starting Backgrounded Processes

![image](https://github.com/user-attachments/assets/21ba300b-56d3-4c5d-ad78-5a6876cd2811)

A process can be started directly in the background by adding `&` at the end of the command. This avoids the need to start the process in the foreground and suspend it later.

* ### Process Exit Codes

![image](https://github.com/user-attachments/assets/5481f3c8-bc53-4aba-8e84-2be36d3d6cac)

The special variable `$?` stores the exit status of the most recently executed command. By checking this value after a process terminates, we can determine its exit code and use the result to complete the challenge and retrieve the flag.
