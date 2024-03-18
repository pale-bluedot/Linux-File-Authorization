# Linux File Authorization

## Objective
The research team at my organization needs to update the file permissions for certain files and directories within the projects directory. The permissions do not currently reflect the level of authorization that should be given. Checking and updating these permissions will help keep their system secure. To complete this task, I performed the following tasks:

### Skills Learned
- Utilize Linux commands to modify permissions set for directories in the file system
- Proficiency in analyzing and interpreting directory permissions.
- Ability to generate and recognize levels of authorization.
- Enhanced knowledge of security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used
- Linux Command Line

## Steps

### 1. Check file and directory details
The following code demonstrates how I used Linux commands to determine the existing permissions set for a specific directory in the file system.

![linux1](https://github.com/pale-bluedot/Linux-File-Authorization/assets/72536144/7165bcb6-28f7-4a79-9473-78462650b530)

*Ref 1: Linux Command*

#### 1a. Describe the permissions string
The 10-character string can be deconstructed to determine who is authorized to access the file and their specific permissions. The characters and what they represent are as follows:
- **1st character**: This character is either a `d` or hyphen (`-`) and indicates the file type. If it’s a `d`, it’s a directory. If it’s a hyphen (`-`), it’s a regular file.
- **2nd-4th characters**: These characters indicate the read (`r`), write (`w`), and execute (`x`) permissions for the user. When one of these characters is a hyphen (`-`) instead, it indicates that this permission is not granted to the user.
- **5th-7th characters**: These characters indicate the read (`r`), write (`w`), and execute (`x`) permissions for the group. When one of these characters is a hyphen (`-`) instead, it indicates that this permission is not granted for the group.
- **8th-10th characters**: These characters indicate the read (`r`), write (`w`), and execute (`x`) permissions for other. This owner type consists of all other users on the system apart from the user and the group. When one of these characters is a hyphen (`-`) instead, that indicates that this permission is not granted for other.


### 2. Change file permissions
The organization determined that other shouldn't have write access to any of their files. To comply with this, I referred to the file permissions that I previously returned. I determined `project_k.txt` must have the write access removed for other.

The following code demonstrates how I used Linux commands to do this:

![linux2](https://github.com/pale-bluedot/Linux-File-Authorization/assets/72536144/2b2f40f5-6ffb-4be5-8fcb-339d0256f08d)

*Ref 2: Linux Command*

### 3. Change file permissions on a hidden file
The research team at my organization recently archived `project_x.txt`. They do not want anyone to have write access to this project, but the user and group should have read access. 

The following code demonstrates how I used Linux commands to change the permissions:

![linux3](https://github.com/pale-bluedot/Linux-File-Authorization/assets/72536144/ff65e683-47d4-4e59-9549-125acf15d37e)

*Ref 3: Linux Command*

### 4. Change directory permissions
My organization only wants the `researcher2` user to have access to the `drafts` directory and its contents. This means that no one other than `researcher2` should have execute permissions.

The following code demonstrates how I used Linux commands to change the permissions:

![linux4](https://github.com/pale-bluedot/Linux-File-Authorization/assets/72536144/5a6a3133-de09-46fb-baad-2f359ea69d0b)

*Ref 4: Linux Command*

