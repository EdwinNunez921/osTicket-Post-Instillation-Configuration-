<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Configuration Steps</h2>

<h2>Step 1: Configure Admin Panel and Add Roles</h2>

<p>
<img src="https://github.com/user-attachments/assets/5c7e3226-1d94-4375-b279-a6cb5e39dbcc" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open Microsoft Edge on the Windows VM and navigate to:
http://localhost/osTicket/scp/login.php

Log in using the admin credentials you set during the osTicket setup process.

Once logged in, confirm that you are in the Admin Panel. If not, click the Admin Panel link in the upper right-hand corner.

In the Admin Panel:

Click Agents in the top navigation menu.
Select Roles from the dropdown.
To add a new role:

Click Add Role.
Enter a name for the role (e.g., "Support Admin" or any name of your choice).
Configure Permissions:

Click the Permissions tab.
Under Tickets, Tasks, and Knowledgebase, check every permission.
Once all permissions are selected, click Add Role to save the new role.

This step ensures the role has full administrative capabilities for managing tickets, tasks, and the knowledge base.
</p>
<br />

<h2>Step 2: Create a New Department in the Admin Panel</h2>

<p>
<img src="https://github.com/user-attachments/assets/9a615b2f-5729-4a9a-a60e-b86646e73de5" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the osTicket Admin Panel, click Agents in the top navigation menu.

From the dropdown, select Departments.

To add a new department:

Click Add New Department.
For Support (default department level), change it to Top-Level Department.
Name the department Sysadmins.
Scroll down to review any additional settings if necessary.

Click Create Department to save the new department.

This step establishes a dedicated department for system administrators to manage tickets effectively.
</p>
<br />

<h2>Step 3: Create a New Team in the Admin Panel</h2>

<p>
<img src="https://github.com/user-attachments/assets/a277d2fc-785d-4348-b5ef-ba3591430c58" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the osTicket Admin Panel, click Agents in the top navigation menu.

From the dropdown, select Teams.

To add a new team:

Click Add New Team.
Enter a name for the team (e.g., "Support Team" or any name you prefer).
Review the team settings as needed.

Click Create Team to save the new team.

This step helps organize agents into teams for better ticket management and collaboration.
</p>
<br />

<h2>Step 5: Update User Settings in the Admin Panel</h2>

<p>
<img src="https://github.com/user-attachments/assets/d64124bb-d004-4a9b-b58e-6657c75ea0c5" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the osTicket Admin Panel, click on Settings in the top navigation menu.

From the dropdown, select Users.

Locate the option labeled Registration Required.

Ensure the checkbox next to Registration Required is unchecked.

Click Save Changes to confirm the update.

This configuration allows users to submit tickets without requiring prior registration, streamlining the support process.
</p>
<br />

<h2>Step 6: Add New Agents in the Admin Panel</h2>

<p>
<img src="https://github.com/user-attachments/assets/d86f2a3e-611f-4cf6-9400-c56624822a22" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate to Agents:
In the admin panel, click on Agents from the menu, then select Add New Agents.

Fill Out Agent Details:
Enter the required information for the new agent.

Set Password:

Click on Set Password.
Uncheck the box for auto-generated passwords.
Manually set a secure password for the agent.
Assign Access for the First Agent:

Under Access, assign the agent to the Sysadmins department.
For Select Role, assign the Supreme Admin role.
For Teams, add the agent to the Online Banking team.
Click Create to save.
Add a Second Agent:

Repeat the process to add a second agent.
Fill out their information, set a password, and uncheck the auto-generated box.
Assign them to the Support department.
Ensure they have All Access permissions.
Click Create to save.
</p>
<br />

<h2>Step 7: Add Members to Teams</h2>

<p>
<img src="https://github.com/user-attachments/assets/8bc4b168-4fed-40c1-9806-6add187b4fc6" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate to Teams:
In the admin panel, click on Teams from the menu.

Select Members:

Click on the Members tab under the desired team.
Locate and select Jane Doe from the list of available agents.
Add Member:

Click Add to include Jane Doe as a team member.
Save Changes:

After adding the member, click Save Changes to apply the updates.
</p>
<br />

<h2>Step 8: Add a User in the Agent Panel</h2>

<p>
<img src="https://github.com/user-attachments/assets/67286883-ce0c-4f05-94d5-a7d7546fd5d4" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate to the Agent Panel:
Log in to the agent panel and click on Users in the menu.

Add User:

Click on Add User.
Fill out the required information, such as the user's name, email address, and any other relevant details.
Save User:

Once all the information is completed, click Save to add the user to the system.
</p>
<br />

<h2>Step 9: Add SLA Plans in the Admin Panel</h2>

<p>
<img src="https://github.com/user-attachments/assets/9f2a2c7e-5cb0-4918-bf75-59d711ecf6ef" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate to SLA Management:

Log in to the Admin Panel.
Click on Manage in the menu.
Select SLA.
Add SLA Plans:

Click Add New SLA Plan for each SLA type.
SLA Plan 1:
Name: Sev-A
Grace Period: 1 hour
Schedule: 24/7
Click Add Plan.
SLA Plan 2:
Name: Sev-B
Grace Period: 4 hours
Schedule: 24/7
Click Add Plan.
SLA Plan 3:
Name: Sev-C
Grace Period: 8 hours
Schedule: Monday - Friday 8am - 5pm with U.S. Holidays
Click Add Plan.
Verify:

Confirm that all SLA plans have been added successfully and appear in the SLA list.
</p>
<br />

<h2>Step 10: Add Help Topics in the Admin Panel</h2>

<p>
<img src="https://github.com/user-attachments/assets/a1ca44c4-02cf-4e13-a6fd-fa3fc497a132" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate to Help Topics Management:

Log in to the Admin Panel.
Click on Manage in the menu.
Select Help Topics.
Add New Help Topics:

Help Topic 1:

Name: Business Critical Outage
Parent Topic: Report a Problem
Click Add Topic.
Help Topic 2:

Name: Personal Computer Issues
Parent Topic: Report a Problem
Click Add Topic.
Help Topic 3:

Name: Equipment Request
Parent Topic: General Inquiry
Click Add Topic.
Help Topic 4:

Name: Password Reset
Parent Topic: Report a Problem
Click Add Topic.
Help Topic 5:

Name: Other
Parent Topic: General Inquiry
Click Add Topic.
Verify:

Ensure that all the help topics have been added successfully and are listed under the appropriate parent topics.
</p>
<br />
