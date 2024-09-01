# File permissions in Linux

## Project description

The goal of this project is to ensure users on this team are authorized with the appropriate permissions. 
This is done to reduce the risk of unauthorized access, increasing security. 
If the permissions do not match the authorization given, modifications will need to be made to correct these permissions. 

## Check file and directory details

![image](https://github.com/user-attachments/assets/8ff82ba0-7f82-49ca-9839-66b0b3e490d6)

The `ls -l` command was used to list all the files and directories in the current directory and their permissions. 

Here's a breakdown of the permissions for each file and directory. 

| File/Directory | User Permissions | Group Permissions | Other Permissions |
| ---------------| ---- | ----- | ----- |
| drafts         | read, write and execute | execute | none |
| project_k.txt  | read and write | read and write | read and write |
| project_m.txt  | read and write | read | none |
| project_r.txt  | read and write | read and write | read |
| project_t.txt  | read and write | read and write | read |

## Describe the permissions string

The permissions string is represented by a 10-character string. 

The first letter can either be a `d` to denote a directory or `-` to denote a file. 

The next three letters are the permissions for the user, the owner of the file. 
The next three letters are the permissions for the group, which consists of users. 
And the last three letters are the permissions for other, who are all the other users in the Linux system. 

In each of the "groups" of three letters, the first of these letters is the read permission, a `r` means permissions is present whereas `-` means there are no permissions. 
The second letter is the write permission, a `w` means write permissions is present whereas `-` means there are none. 
And lastly, the third letter is the execute permission, a `x` denotes execute permissions is present whereas `-` means there are no execute permissions. 

## Change file permissions

The organization does not allow other to have write access to any files. 

Since `project_k.txt` has permissions that allow `other` to have write permissions. 
We need to remove that permission using the `chmod o-w project_k.txt` command. 

This command removes the write permissions from the other group for the file `project_k.txt`.

![image](https://github.com/user-attachments/assets/d980d0a7-02c1-4b68-bb3a-325a574e95da)

## Change file permissions on a hidden file

The research team has archived `.project_x.txt`, which is why it’s a hidden file. 
This file should not have write permissions for anyone, but the user and group should be able to read the file. 

We can see hidden files and directories using the `ls -a` command. 

After running `ls -l .project_x.txt`, we can see the following user and group permissions are not correct:
1. It has write permissions for group
2. It doesn't have read permissions for group
3. It has write permissions for the user

![image](https://github.com/user-attachments/assets/74004d08-ef2d-41a1-a968-adac09697cea)

We will correct the permissions using the `chmod u=r,g=r .project_x.txt` command, which explicity sets the user and group permissions to read-only. 

![image](https://github.com/user-attachments/assets/e08e878d-f33a-4213-b857-37a77ebcec4a)

## Change directory permissions

The files and directories in the projects directory belong to the `researcher2` user. Only `researcher2` should be allowed to access the drafts directory and its contents.

For directories, the permission that determines who can access it's contents is the execute permission. 

So, we have to remove the execute permission for the group using the `chmod g-x drafts` command. 

![image](https://github.com/user-attachments/assets/fa5854a2-d1a1-4f2c-a609-a9f27de286d2)

Now, only the user can access the directory `drafts`. Because only the user group has the execute permission. 

## Summary

After auditing the file and directory permissions in the `/home/researcher2/projects` directory, using the `ls -l` command, we access control issues. 
This could lead to unauthorized use of files or directories. 
We promptly rectified these permissions using the `chmod` command. 
