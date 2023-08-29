# post-install-config
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

<h2>Post-Install Configuration Objectives</h2>
<p><ul><li>Configure Help Desk Topic
<li>Configure Service Learning Agreements
<li>Create and Configure Agents & Users
<li>Create and Configure Roles
<li>Create and Configure Departments & Teams
</ul></p>

<h2>Configuration Steps</h2>

<h3>Configuring Roles</h3>
<p>
  Go to the <a href="http://localhost/osTicket/scp/login.php">Help Desk Login Page</a> and sign into osTicket. And Click on the "Admin Panel".</p>
  <img src="https://user-images.githubusercontent.com/142059616/263860964-2c48a574-097d-4965-8999-b6896f626c85.png" height="35%" width="60%" alt="Disk Sanitization Steps"/>
   <img src="https://user-images.githubusercontent.com/142059616/263861665-52927855-dc65-4ef4-b036-28759ef78ee2.png" height="35%" width="60%" alt="Disk Sanitization Steps"/>

</p>
<p>
 "Agents"-->"Roles-->"Add New Role"
  <img src="https://user-images.githubusercontent.com/142059616/263862394-4ddba97f-7723-468a-8b0a-64841a6a7e04.png" height="35%" width="60%" alt="Disk Sanitization Steps"/>
 <ul> <li>In the Defenitions Tab type in any name for the role name. In this case we will use "King Admin"
 </ul>
 <img src="https://user-images.githubusercontent.com/142059616/263863006-6f230c73-ea5c-4692-91b3-fdba0b02d052.png" height="35%" width="60%" alt="Disk Sanitization Steps"/>
  In the Permissions Tab, checkmark <b>All</b> boxes for the three tabs, "Tickets" "Tasks" "Knowledgebase"

</p>
<p>
  Next, we are going to create a department
  <ul>
    <li>Click on the "Departments" tab
    <li>Select "Add New Department"
  </ul>
  <img src="https://user-images.githubusercontent.com/142059616/263865752-26b718aa-00d0-4ada-a07e-8e7d5d8fba68.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
 Create a Department name of your choice (this example uses **System Administrators**).
- Skip everything else for now and click "Create Dept".
<p align=center>
<img src="https://i.imgur.com/Uoji0y5.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

_Next, we'll move onto creating a Team._ <br>
_"Teams allow you to pull Agents from different Departments and organize them to handle a specific issue or user via a Help Topic or Ticket Filter."_
- Currently in the Agents tab, click on the "Teams" category.
- Click "Add New Team".
<p align=center>
<img src="https://i.imgur.com/jmrWFse.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Create a Team name of your choice (this example uses **Level II Support**).
- Click "Create Team".
<p align=center>
<img src="https://i.imgur.com/JyzMjkp.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Currently in the Agents tab, click "Agents" category.
<p align=center>
<img src="https://i.imgur.com/zYQu22H.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Create the required credentials for this user that are in bold:
  - First Name (this example uses **Jane**).
  - Last Name (this example uses **Doe**).
  - Email Address (this example uses **jane.doe@osTicket.com**).
  - Username (this example uses **jane.doe**).
- Click "Set Password" and a windows prompt will appear:
  -   Uncheck "Send the agent a password reset email".
  -   Create a password for this user.
  -   Uncheck "Require password change at next login".
  -   Click "Set".
<p align=center>
<img src="https://i.imgur.com/LRAyfYp.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Click on the "Access" tab:
  - Assign this user the Department that we created (this example uses **System Administrators**).
  - Assign this user the Role that we created (this example uses **Supreme Admin**).
- Under Extended Access, assign this user the "Support" department with the "Supreme Admin" role.
- Click "Save Changes".
<p align=center>
<img src="https://i.imgur.com/NyCTS3W.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Click on the "Teams" tab:
  -  Assign this user the Team that we created (this example uses **Level II Support**).
-  Once done, click "Create".
<p align=center>
<img src="https://i.imgur.com/WeM5SEd.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

_Create another Agent following the steps, however assign it to a different Role and Department._</br>
_This example creates Agent **"John Doe"** | Department: **"Level I Support"** | Role: **"View only** | Extended Access: **Support"**_.
<p align=center>
<img src="https://i.imgur.com/ACl29nn.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<hr>

<h3>Creating Users</h3>

- Click on "Agent Panel" on the top-right of the page.
<p align=center>
<img src="https://i.imgur.com/A6lRMQN.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Click on the "Users" tab.
- Click on "Add User".
- Create an Email Address and Full Name for this user (this example uses **karen@osticket.com / Karen Karen**).
- Click "Add User".
<p align=center>
<img src="https://i.imgur.com/jTIRdhl.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/vn9DP8b.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

_Create another user of your choice (this example uses **ken@osticket.com / Ken Ken**)_
<p align=center>
<img src="https://i.imgur.com/H6Cgj0A.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<hr>

<h3>Configuring SLA</h3>

_"SLA Plans or Service Level Agreements, are unlimited in osTicket. The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed."_
- Return to the "Admin Panel".
  - Navigate to "Manage" tab > "SLA".
- Click "Add New SLA Plan".
<p align=center>
<img src="https://i.imgur.com/KSONgtH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Create the following plans:
  - **SEV-A**
    - Grace Period: **1 hour** (_Amount, in hours, before tickets with this SLA will become overdue if not closed in allotted time._)
    - Schedule: **24/7** (_Accounted for all days of the week, even on non-business days_)
  
  - **SEV-B**
    - Grace Period: **4 hours**
    - Schedule: **24/7**

  - **SEV-C**
    - Grace Period: **8 hours**
    - Schedule: **Monday - Friday 8am - 5pm with U.S. Holidays**
- Click "Add Plan" for each.
<p align=center>
<img src="https://i.imgur.com/biqgLPr.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/vLW1yZs.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<hr>

<h3>Configure Help Topics</h3>

_Help Topics will help streamline your end-user’s help desk experience to ensure proper assignment and prompt response to the ticket._
- Currently in the Admin Pangel, navigate to "Manage" tab > "Help Topics".
- Click "Add New Help Topic".
<p align=center>
<img src="https://i.imgur.com/cYxBbIu.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Create Help Topics with the following names:
  - **Business Critical Outage**
  - **Personal Computer Issues**
  - **Equipment Request**
  - **Password Reset**
- "Internal Notes" can be written down for personal use, but not necessary.
- After that, click "Add Topic".
<p align=center>
<img src="https://i.imgur.com/8u6QJRG.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/wVf8qYz.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<hr>
<h2>ALL DONE!!😆  </h2>
