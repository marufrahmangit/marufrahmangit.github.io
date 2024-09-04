---
layout: default
---

[🏠 home](../)

<h1 style="text-align: center;">System Administration: Employee and Machine Data Retrieval using SQL</h1>

# Scenario
As a system administrator, you need to get specific information about employees, their machines, and the departments they’re in. Your team needs this data to perform various tasks, such as running updates, posting a privacy notice in certain departments, and sending an alert to an employee with an issue on a machine.

[Project reference](https://www.coursera.org/learn/linux-and-sql/home/welcome)

# List all organization machines
Get a list of all organization machines and their operating systems.

![image](https://github.com/user-attachments/assets/03fad05f-6d60-416e-8732-2056e3ea5a22)

# Retrieve a list of the machines with OS 2
Obtain a list of all machines with the `OS 2` operating system because these machines need an update.

![image](https://github.com/user-attachments/assets/b6baba53-e7c8-4a46-8aed-150b4c96b20e)

# List employees in the Finance and Sales departments
Retrieve a list of all the employees in the `Finance` and `Sales` departments to obtain their office numbers. A notice about handling confidential financial information will be posted to these offices.

1. I filtered the rows returned from `department` column in the `employees` table to include only employees from the `Finance` department.

![image](https://github.com/user-attachments/assets/a57d10e8-dbc8-4c9b-a1ea-8d08ec14d298)

The employee id of the first employee is `1003`

2. I Modified the previous query so that it returns employees who are in the 'Sales'` department.

![image](https://github.com/user-attachments/assets/1a530431-c009-4a28-98e4-b36e7018fee5)

# Identify employee machines using the South office
Your team recently discovered that there are issues with machines in the South building. In this task, you need to obtain certain employee and computer information. A machine in `'South-109'` has an issue. You need to determine which employee uses that computer so you can send them an alert.

1. I identified which employee uses the office in `'South-109'`.

![image](https://github.com/user-attachments/assets/2dbbbbe2-2158-40b5-8ec0-6c81255e00d1)

user id:1010, username:jlansky

2. Your team has determined that there is an issue with all the machines in the South building. Offices in the organization are named with the building name, a hyphen, and the office number in that building (for example, `'South-109'`). Modify the query you used in the previous step so that it returns information on all the employees in the `'South'` building.

![image](https://github.com/user-attachments/assets/1670662c-2fa2-4b55-bc68-f83a4dc2c0eb)

The first employee listed in the South building belong to the `Finance` department.

# Retrieve employee device data
Retrieve login attempts after the date `'2022-05-09'`

![image](https://github.com/user-attachments/assets/6d82656b-881e-49db-b76a-28ed44d21fb7)

Next, retrieve data for login attempts that were made on or after `'2022-05-09'`

![image](https://github.com/user-attachments/assets/6dbd482d-d93b-429f-b3dd-3c908e977fd8)

# Retrieve employee device data
I need to narrow the focus of the search. Login attempts made after `2022-05-11` shouldn't be included. I need to return results between `'2022-05-09'` and `'2022-05-11'`.

![image](https://github.com/user-attachments/assets/25823552-ef44-4dc9-b126-1b17a7e3256e)

# Investigate logins at certain times
First, your organization's typical work hours begin at 07:00:00. 
I need to retrieve all login attempts made before `07:00:00` to learn more about the users who are logging in outside of typical hours.

![image](https://github.com/user-attachments/assets/ab5bf369-2bd2-4280-b91f-0c92f5106aa7)

The username of the fifth record is `eraab`.

The query in the previous step returned more results than required. I need to return logins between '06:00:00' and '07:00:00'.

![image](https://github.com/user-attachments/assets/3ad40dfe-0bd0-427c-b379-4fd1e1a857bc)

The earliest login time between the time range is `06:01:31`.

# Investigate logins by event ID
I need to investigate login attempts based on event ID numbers. With this query, you want to return only the `event_id`, `username`, and `login_date` fields from the `log_in_attempts` table.

I need to return the login attempts with `event_id` greater than or equal to `100`.

![image](https://github.com/user-attachments/assets/863efad3-a203-439d-95e7-3e3879e8edda)

The login date of the third result is `2022-05-09`.

Next, I need to modify the query to return only login attempts with `event_id` between `100` and `150`.

![image](https://github.com/user-attachments/assets/e9984bc5-880b-4dc4-8a10-3484ad9eebb0)

The username of the seventh result is `tmitchel`.
