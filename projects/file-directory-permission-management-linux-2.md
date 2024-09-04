---
layout: default
---

[🏠 home](../)

<h1 style="text-align: center;">File and Directory Permission Management on Linux OS(Part 2)</h1>

# Scenario
As an analyst, you must examine and manage the permissions on the files in the `/home/researcher2/projects` directory for the `researcher2` user.

The `researcher2` user is part of the `research_team` group.

You must check the permissions for all files in the directory, including any hidden files, to make sure that permissions align with the authorization that should be given. When it doesn't, you must change the permissions.

Here’s how you’ll do this task: First, you’ll check the user and group permissions for all files in the `projects` directory. Next, you’ll check whether any files have incorrect permissions and change the permissions as needed. Finally, you’ll check the permissions of the `/home/researcher2/projects/drafts` directory and modify these permissions to remove any unauthorized access.

[Project reference](https://www.coursera.org/learn/linux-and-sql/home/welcome)

# Check file and directory details
Navigate to the projects directory:

![image](https://github.com/user-attachments/assets/633755b2-30e2-4e7d-849a-1d2843643bda)

List the contents and permissions of the projects directory:

![image](https://github.com/user-attachments/assets/6d7e8215-a8e8-4518-b98a-24549f97af1c)

A hidden file `.projects.txt.`, a `drafts` folder, and a bunch of .txt files are listed along with their permissions.

### permission explained
*A 10-character string begins each entry and indicates how the permissions on the file are set. For instance, a directory with full permissions for all owner types would be `drwxrwxrwx`*.
- The `1st` character indicates the file type. The d indicates it’s a directory. When this character is a hyphen (-), it's a regular file.
- The `2nd-4th` characters indicate the read (r), write (w), and execute (x) permissions for the user. When one of these characters is a hyphen (-) instead, it indicates that this permission is not granted to the user.
- The `5th-7th` characters indicate the read (r), write (w), and execute (x) permissions for the group. When one of these characters is a hyphen (-) instead, it indicates that this permission is not granted for the group.
- The `8th-10th` characters indicate the read (r), write (w), and execute (x) permissions for the owner type of other. This owner type consists of all other users on the system apart from the user and the group. When one of these characters is a hyphen (-) instead, that indicates that this permission is not granted for other.

# Change file permissions
Check whether any files in the projects directory have write permissions for the owner type of other:

![image](https://github.com/user-attachments/assets/ee199c22-8eca-44d7-9bc8-6e7100ae41ca)

*The second last character `w` shows that the owner type has write permissions.*

Change the permissions of the file identified in the previous step so that the owner type of other doesn’t have write permissions: `chmod o-w <file name>`

![image](https://github.com/user-attachments/assets/6e472aaf-316f-42c6-bee6-d9f4c4c4610f)

*The highlight in yellow shows `w` (write) permission is removed for the file.*

The file project_m.txt is a restricted file and should not be readable or writable by the group or other; only the user should have these permissions on this file. List the contents and permissions of the current directory and check if the group has read or write permissions: 

![image](https://github.com/user-attachments/assets/7bec8a7c-f6d7-497a-81ce-8ee47cb5167e)

*The group has read permission on the file as shown by the second `r` character in the highlighted yellow box.*

Change permissions of the project_m.txt file so that the group doesn’t have read or write permissions: 

![image](https://github.com/user-attachments/assets/c6478c04-32c3-49d7-9185-3f0c0a76c4c7)

*The read permission `r` has been removed (highlighted in yellow).*

# Change file permissions on a hidden file
Check the permissions of the hidden file `.project_x.txt`.

![image](https://github.com/user-attachments/assets/571847ac-7b41-4da4-b0d3-bd48d170f8b5)

The user and the group have incorrect `write` permissions. Change it so that the user and the group can read, but not write to the file: `chmod u-w,g-r,g+r <file name>`

![image](https://github.com/user-attachments/assets/9fe30b1f-ca27-45a7-a800-1f0f6693d74a)

*The green highlighted box shows the command and the yellow highlighted box shows the changed permission.*

# Change directory permissions
Remove the execute permission for the group from the `drafts` directory: `chmod g-x drafts`

![image](https://github.com/user-attachments/assets/1e2fe3d7-64ad-40fa-96f5-6542cd85fc68)

*The green highlighted box shows the command and the yellow highlighted box shows the changed permission.*
