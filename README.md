<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket: Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines / Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 (22H2)

<h2>Post-Install Configuration Objectives</h2>

- Azure Virtual Machine
- Remote Desktop Application on either Windows or [MacOS](https://apps.apple.com/us/app/windows-app/id1295203466?mt=12)
- Installed osTicket Instance (this instruction set is using v1.15.8)

<h2>Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/OxWlEW9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
  
🔐 Step 1: Access Panels
  
-	**Admin/Analyst Login Page:** http://localhost/osTicket/scp/login.php
-	**End Users Ticket Submission URL:** http://localhost/osTicket

💡 The Admin Panel (/scp) is for help desk agents/admins. The End User Panel (/osTicket) is for customers submitting tickets.

</p>
<br />

<p>
<img src="https://i.imgur.com/9sfjTYy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

🧑‍💼 Step 2: Configure Roles (Permission Groups)

- Navigate to: **Admin Panel → Agents → Roles**

- Click **Add New Role**
	- Name: **Supreme Admin**
- Click **Permissions**
	- Check All Permissions under the **Tickets** Tab
 	- Check All Permissions under the **Tasks** Tab
- Click **Add Role** to Complete

</p>
<br />

<p>
<img src="https://i.imgur.com/eR33QJv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

🏢 Step 3: Configure Departments

- Navigate to: **Admin Panel → Agents → Departments**

- Click **Add New Department**
	- Name: **SysAdmins**
 		- Leave other fields in their current setup for now
   		- Click **Create Dept** 	

📌 Departments, for example: **SysAdmins**, **Help Desk**, **Networking**, are created for better ticket routing and visibility and determine who can view/respond to which tickets.

</p>
<br />

<p>
<img src="https://i.imgur.com/yMcTctX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

👥 Step 4: Create Teams

- Navigate to: **Admin Panel → Agents → Teams**

- Click **Add New Team**
	- Name: **Online Banking**
 		- Leave other fields in their current setup for now
   		- Click **Create Team** 	

📌 Teams allow for Cross-Department Collaboration. You can add members from different departments to specific teams.

</p>
<br />

<p>
<img src="https://i.imgur.com/PvEMXDf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

⚙️ Step 5: Allow Ticket Creation for All Users

- Navigate to: **Admin Panel → Settings → User**
  - 🔲 Uncheck: **Require registration and login to create tickets**

✅ This allows unregistered users to submit tickets through the public form.

</p>
<br />

<p>
<img src="https://i.imgur.com/W9WRc4G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

👩‍💻 Step 6: Add Agents (Staff Members)

- Navigate to: **Admin Panel → Agents → Add New**

- 1st Agent to Create:
	- Name: **Jane Doe**
 	- Email: **jane.doe@capsulecorp.com**
  	- Username: **jane**
  		- Click **Set Password**
  		- Uncheck **Send the agent a password reset email** (for the purposes of this demonstration)
  		- Set new password as **Password1** and confirm
  		- Uncheck **Require password change at next login**
  	 	- Set Password
  	- Click **Access**
  		- Assign the Primary Department as **SysAdmins** and the Role under **Supreme Admin**
  	- Click **Teams**
  		- Assign to the **Online Banking** Team and click **Add**
  	 - Create
  
- 2nd Agent to Create:
	- Name: **John Doe**
 	- Email: **john.doe@capsulecorp.com**
  	- Username: **john**
  		- Click **Set Password**
  		- Uncheck **Send the agent a password reset email** (for the purposes of this demonstration)
  		- Set new password as **Password1** and confirm
  		- Uncheck **Require password change at next login**
  	 	- Set Password
  	- Click **Access**
  		- Assign the Primary Department as **Support** and the Role under **View Only**
  	 - Create

</p>
<br />

<p>
<img src="https://i.imgur.com/k6VYfpV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

👨‍👩‍👧 Step 7: Add Users

- Navigate to: **Agent Panel → Users**

- Click **Add User**

- User to Create:
	- Email Address: **mai@capsulecorp.com**
 	- Full Name: **Mai**
    	- Add User

🗣️ Users (or customers, clients, etc.) submit tickets to the system.

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

⏱️ Step 8: Configure SLA Policies

- Navigate to: **Admin Panel → Manage → SLA**

- Create SLA plans:
  - **Sev-A:** Grace Period 1 hour, Schedule 24/7
  - **Sev-B:** Grace Period 4 hours, Schedule 24/7
  - **Sev-C:** Grace Period 8 hours, Schedule Business Hours

📅 SLA policies help enforce ticket response deadlines.

</p>
<br />

<p>
<img src="https://i.imgur.com/k4HOihJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

⏱️ Step 8: Configure SLA (Service Level Agreement) Policies

- Navigate to: **Admin Panel → Manage → SLA**

- Click **Add New SLA Plan**

- Create SLA plans:
  	- Name: **Sev-A**
  		- Grace Period: **1 hour**
  		- Schedule: **24/7**
  	 	- Add Plan
  		- 🔴 Critical Business Impact – your business has experienced a significant loss or degradation of services, requiring immediate attention.
  	  
  	- Name: **Sev-B**
  		- Grace Period: **4 hours**
  		- Schedule: **24/7**
  	 	- Add Plan
  		- 🟡 Moderate Business Impact – you have a loss or degradation of services, but your organization can still function.
 
  	- Name: **Sev-C**
  		- Grace Period: **8 hours**
  		- Schedule: **Monday - Friday 8A - 5P with U.S. Holidays** (Business Hours)
  	 	- Add Plan
  		- ⚪️ Minimum Business Impact – you have an issue, but it has a small impact on your business.

🏁 SLA policies help enforce ticket response deadlines and vary based on the agreement between vendor and customer.

</p>
<br />

<p>
<img src="https://i.imgur.com/7W0uufL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

❓ Step 9: Create Help Topics

- Navigate to: **Admin Panel → Manage → Help Topics**

- Click **Add New Help Topic**

- Create new help topics
	- Topic: **Business Critical Outage**
 		- Parent Topic: **Report a Problem**
   		- Add Topic
       
	- Topic: **Personal Computer Issues**
 		- Parent Topic: **Report a Problem**
   		- Add Topic
       
   	- Topic: **Equipment Request**
   		- Parent Topic: **General Inquiry**
   	 	- Add Topic
   	    
   	- Topic: **Password Reset**
   		- Parent Topic: **Report a Problem**
   	 	- Add Topic
   	    
   	- Topic: **Other**
   		- Parent Topic: **General Inquiry**
   	 	- Add Topic               

🧾 Help Topics guide users to categorize their tickets properly.

</p>
<br />
