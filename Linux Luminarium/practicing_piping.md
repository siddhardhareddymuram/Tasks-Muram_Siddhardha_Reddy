# cryptonite_taskphase1_anna
## Module 6 : Practicing Piping

- ### Redirecting output
![image](https://github.com/user-attachments/assets/6f13fac0-a217-48cd-8e27-4710f7b7312d)
Using `>` to redirect the output **PWN** to the **COLLEGE** file

- ### Redirecting more output
![image](https://github.com/user-attachments/assets/6650a0c5-b550-4151-8cbd-5736e40b985d)
Here, we redirect the output of `/challenge/run` which is the flag, to the file **myflag**

- ### Appending output
![image](https://github.com/user-attachments/assets/e4638333-e19f-442b-a058-c93dd36e825f)
![image](https://github.com/user-attachments/assets/fbfd5395-6ec2-4bbe-a157-da03fdaaae3d)
Here, `/challenge/run` writes the first half of the flag directly to the file when using `>`. For the second half, we need to use `>>` to append the second half into the same file.

- ### Redirecting errors
![image](https://github.com/user-attachments/assets/97fbcbee-b675-42e3-9452-f171224a1b63)
In this challenge, we redirected the instructions of the `/challenge/run` command to the **instructions** file and the output to the **myflag** file, giving us the flag.

- ### Redirecting input
![image](https://github.com/user-attachments/assets/8013893d-5668-40cd-9725-3291ad9ac07f)
First we redirect the ouput **CHALLENGE** into the **PWN** file. This file input is then redirected to `/challenge/run` by using `<`

- ### Grepping stored results
![image](https://github.com/user-attachments/assets/ee8b93be-609e-4458-8c0b-2a7d2b9360a7)
Here, we first redirect the output of `/challenge/run` to the file `/tmp/data.txt` and then `grep` that data to get the flag.

- ### Grepping live output
![image](https://github.com/user-attachments/assets/e8439aac-12e0-4038-b04e-74f2d9288d64)
We can directly redirect output and grep the input in one line by using the `|` pipe operator. Here, we grep the output of `/challenge/run` to get the flag.

- ### Grepping errors
![image](https://github.com/user-attachments/assets/1b6fb6ba-c391-4ad4-8f16-101726ae6a4d)
Here, we are using `2>&1` to redirect the standard error to standard output and then grepping the combined stderr and stdout to get the flag.

- ### Duplicating piped data with tee
![image](https://github.com/user-attachments/assets/cf734f88-10ef-4cd5-9a6f-c10ed651e0af)
Used `tee` to intercept pwn and get its secret code and pipe it into `/challenge/college`

- ### Writing to multiple programs
![image](https://github.com/user-attachments/assets/7dbcadf6-6e53-4be7-a4df-4514fb4e5816)
Using `tee >()` we can write the command output as input to the respective programs

- ### Split-piping stderr and stdout
![image](https://github.com/user-attachments/assets/a9e6fe69-695b-44c5-9788-c346db013baf)
Using `2>` and `>()` together to pipe stderr while using `1>` and `>()` to pipe stdout and getting the flag in the process.