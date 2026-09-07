## Module 9: Perceiving Permissions

* ### Changing File Ownership

![image](https://github.com/user-attachments/assets/db98912b-b0cb-45a6-b49d-a854087f826a)

![image](https://github.com/user-attachments/assets/923d8ea6-5d5a-4dd2-aea2-2cebb12d251b)

The `chown` command is used to change the owner of a file. This can be useful when a file is owned by `root` and needs to be accessed by another user. In this challenge, we changed the ownership of the flag file to gain the required access.

* ### Groups and Files

![image](https://github.com/user-attachments/assets/c103393e-672f-4a7e-9c5a-1cea9b62126d)

The `chgrp` command is used to change the group associated with a file. While `chown` can modify the file owner, `chgrp` specifically changes its group ownership.

* ### Fun with Group Names

![image](https://github.com/user-attachments/assets/700a33eb-b85d-42c5-a929-fc2821eb69c4)

This challenge focuses on working with group names and understanding how group membership affects access to files and resources.

* ### Changing Permissions

![image](https://github.com/user-attachments/assets/edac932c-2bdd-4f05-a9b4-4d30f126b268)

Linux file permissions determine who can perform specific operations on a file. The symbols `u`, `g`, and `o` represent the **user (owner), group, and others**, which define **WHO** the permission applies to. The symbols `r`, `w`, and `x` represent **read, write, and execute**, which define **WHAT** actions are allowed.

* ### Executable Files

![image](https://github.com/user-attachments/assets/741502af-0138-43ff-b381-8af9b58df942)

A file needs execute permission in order to be run as a program. In this challenge, we modify the execute permission of `/challenge/run` so that it can be executed successfully.

* ### Permission Tweaking Practice

![image](https://github.com/user-attachments/assets/90715bca-1d96-4b60-9367-6e82edca5d13)

![image](https://github.com/user-attachments/assets/db7afcfb-819b-4a69-9b1a-b64b93691d99)

![image](https://github.com/user-attachments/assets/27b0277a-a092-4cb7-aa18-56f5727db066)

![image](https://github.com/user-attachments/assets/2014597b-70b1-4590-81f6-a54922f68013)

![image](https://github.com/user-attachments/assets/42de4de3-d9f5-43ff-946f-c513126e7625)

![image](https://github.com/user-attachments/assets/7540aeae-54fe-4f48-9043-47f3948ae332)

![image](https://github.com/user-attachments/assets/98180083-c4ff-4b8a-ace5-5c6928a87fd8)

![image](https://github.com/user-attachments/assets/7016ccd1-49ab-4727-a93a-b4e3a702e31d)

![image](https://github.com/user-attachments/assets/edf7047e-5fd3-4759-b4bf-754037b1564f)

![image](https://github.com/user-attachments/assets/3e3d1c4d-feb1-4587-873e-df4dbcb001d4)

This section provides hands-on practice with modifying file permissions. Different combinations of `r`, `w`, and `x` permissions are applied to the owner, group, and other users to achieve the required access configuration.

* ### Permissions Setting Practice

![image](https://github.com/user-attachments/assets/bcac0cb9-9c96-40dd-9e4a-ce9a5a68bc75)

![image](https://github.com/user-attachments/assets/3fa668d8-0fda-4c8a-b34a-a84a728ef27a)

![image](https://github.com/user-attachments/assets/cba79a5b-4a2c-4edf-a4dd-4208b70b18bd)

![image](https://github.com/user-attachments/assets/c1d8557f-55b1-47b9-afef-6908ab4c98fe)

![image](https://github.com/user-attachments/assets/b2d29082-8c7e-453c-a088-e886067c2278)

![image](https://github.com/user-attachments/assets/bde63aca-ebc4-44ee-8e2b-c5e09c8a6949)

![image](https://github.com/user-attachments/assets/21292d4f-8357-4b4a-8620-3ea3ab724b22)

![image](https://github.com/user-attachments/assets/27c21778-c501-416c-9b6d-623e48760eea)

![image](https://github.com/user-attachments/assets/b8a94508-9643-40b0-817a-00d8b102de19)

The `=` operator can be used to explicitly set permissions, replacing the existing permission configuration with the one specified in the command.

* ### The SUID Bit

![image](https://github.com/user-attachments/assets/8d53783d-8355-4541-82e8-e84b1e02428e)

The SUID (Set User ID) bit is a special file permission that causes an executable program to run with the permissions of its file owner rather than the permissions of the user who launched it. This is an important Linux permission feature and is commonly encountered when working with privileged programs.
