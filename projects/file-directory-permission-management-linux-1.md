---
layout: default
---

[🏠 home](../)

<h1 style="text-align: center;">File and Directory Permission Management on Linux OS (Part 1)</h1>

# Scenario
As an analyst, you need to
- locate and analyze the information of certain files,
- ensure that the `/home/analyst` directory is properly organized

[Project reference](https://www.coursera.org/learn/linux-and-sql/home/welcome)

# Locate and analyze files

### Get the current directory information
Display your working directory and the names of the files and directories in the current working directory.
`pwd` to display working directory > `ls` to list all directories

![image](https://github.com/user-attachments/assets/5fe9b640-7a2d-4582-aa78-4dca0a4f0409)

### Change directory and list the subdirectories
Navigate to a `/home/analyst/reports` directory and determine the subdirectories it contains.

![image](https://github.com/user-attachments/assets/a4a34be1-de5f-494b-a732-04b476cc2267)

*Subdirectory: `users`*

### Locate and read the contents of a file
Navigate to a `/home/analyst/reports/users` and read the contents of a file it contains.
`cd users` > `ls` > `cat <file>`

![image](https://github.com/user-attachments/assets/88eca8f2-af84-4790-80c9-d63986b65fa6)

### Navigate to a directory and locate a file
Navigate to `/home/analyst/logs`, display the name of the file it contains, and display the first **10** lines of this file.
`cd logs` > `ls` > `head <file>`

![image](https://github.com/user-attachments/assets/2260a7fc-0146-43a9-a94a-a0c37af27c53)

### Search for error messages in a log file
Navigate to the `/home/analyst/logs` directory and report on the error messages in the `server_logs.txt` file.
`cd logs` > `ls` > `grep error <file>`

![image](https://github.com/user-attachments/assets/bcfcf9f6-f08e-4e94-92ee-d03c3721c759)

### Find files containing specific strings
- Navigate to the `/home/analyst/reports/users` directory and search for user data files that contain a specific string in their names.
- List only the files containing the string `Q1` in their names: `ls | grep "Q1"`
- List the files that contain the word `access` in their names: `ls | grep "access"`

![image](https://github.com/user-attachments/assets/91eb86b5-2ead-4086-ad56-eb732eec31eb)

### Search for information contained in user files
- Display the files in the `/home/analyst/reports/users` directory. 
- Search the `Q2_deleted_users.txt` file for the username `jhill`: `cat Q2_deleted_users.txt | grep "jhill"`
- Search the `Q4_added_users.txt` file to list the users who were added to the `Human Resources` department: `cat Q4_added_users.txt | grep "Human Resources"`

![image](https://github.com/user-attachments/assets/cac55ad5-73ec-4546-a15c-ce578f836577)


# Manage directories and files

### Create a new directory
Create a new subdirectory called logs in the `/home/analyst` directory and list the contents of the `/home/analyst` directory to confirm that you’ve successfully created the new logs subdirectory.
`mkdir logs` > `ls`:

![image](https://github.com/user-attachments/assets/2f6ce4ae-4096-49b0-a41d-9eaf9b72a7e9)

### Remove a directory
Remove the `/home/analyst/temp` directory and list the contents of the `/home/analyst` directory to confirm that you have removed the temp subdirectory.
`rmdir temp` > `ls`:

![image](https://github.com/user-attachments/assets/d1845655-2a10-4935-ac60-78a78e71f578)

### Move a file
Navigate to the `/home/analyst/notes` directory. Move the `Q3patches.txt` file from the `/home/analyst/notes` directory to the `/home/analyst/reports` directory. List the contents of the `/home/analyst/reports directory` to confirm that you have moved the file successfully.
`cd notes` > `ls` > `mv <file> <directory>` > `cd .. ` > `cd reports` > `ls`

![image](https://github.com/user-attachments/assets/49460ad9-ade4-40c5-a841-368679d1cd0a)

### Remove a file
Remove the `tempnotes.txt` file from the `/home/analyst/notes` directory and list the contents of the `/home/analyst/notes` directory to confirm that you’ve removed the file successfully.
`cd ..` > `cd notes` > `ls` > `rm <file>` ls

![image](https://github.com/user-attachments/assets/5e9babc9-08cd-4804-9ac7-dd13f4f2672b)


### Create a new file
Create a file named tasks.txt in the /home/analyst/notes directory that you’ll use to document completed tasks. 
`touch <file>` > `ls`

![image](https://github.com/user-attachments/assets/95b6e5c7-64d3-4a79-96b2-f1c301186f27)

### Edit a file
Edit the `tasks.txt file` and add a note describing the tasks you’ve completed.
`nano <tasks.txt>` to open the editor > write content > `CTRL + X` to close the editor > `Y` to save content > Press `Enter` to confirm save and close > `cat <file> to read content`

![image](https://github.com/user-attachments/assets/05a21cfa-4a8a-409a-a616-0828c9e4f39c)
