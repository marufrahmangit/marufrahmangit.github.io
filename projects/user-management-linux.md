---
layout: default
---

[🏠 home](../)

<h1 style="text-align: center;">User Management in Linux</h1>

# Scenario
A new employee with the username `researcher9` joined the organization. As an analyst, you have to add them to the system and continue to manage their access during their time with the organization.

## Tasks
- Add a new employee to the system and then to their primary group.
- Make the employee the owner of a file related to a particular project.
- Add the new employee to a supplementary group.
- Delete the employee from the system.

[Project reference](https://www.coursera.org/learn/linux-and-sql/home/welcome)

# Add a new user
Add a new employee with the username `researcher9` to the system and then to their primary group called `research_team`.
- added user: `sudo useradd researcher9`
- modify user to set primary group: `sudo usermod -g research_team`
  
![image](https://github.com/user-attachments/assets/c5bd2fbd-a42b-44d5-b7cd-03e6893682d1)

# Assign file ownership
Make `researcher9` the owner of `/home/researcher2/projects/project_r.txt`.
`sudo chown researcher9 project_r.txt`

![image](https://github.com/user-attachments/assets/26abf060-9a66-4985-9096-466c602aff59)

# Add the user to a secondary group
A couple of months later, this employee's role at the organization has changed, and they are working in both the Research and the Sales departments. Add `researcher9` to a secondary group (`sales_team`). Their primary group is still `research_team`.
`sudo usermod -G sales_team researcher9`

![image](https://github.com/user-attachments/assets/84d48f6c-dda3-4449-a515-e0b3220cea57)

# Delete a user
A year later, `researcher9`, decided to leave the company. In this task, you must remove them from the system.
`sudo userdel researcher9`. This removed the user but also prompted a message (yellow line on the screenshot).
`sudo groupdel researcher9`. This deleted the group that is no longer required.


![image](https://github.com/user-attachments/assets/5503934f-975d-4867-8132-7d4c245d2204)

