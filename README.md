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
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

🧑‍💼 Step 2: Configure Roles (Permission Groups)

- Navigate to: **Admin Panel → Agents → Roles**

-	Add a new role, Supreme Admin, to define permission levels for agents.

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

🏢 Step 3: Configure Departments (Ticket Visibility)

- Navigate to: **Admin Panel → Agents → Departments**

- Examples:
  - SysAdmins
  - Help Desk
  - Networking

📌 Departments determine who can view/respond to which tickets.

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

👥 Step 4: Create Teams (Cross-Department Collaboration)

- Navigate to: **Admin Panel → Agents → Teams**

- Create a team like Online Banking and assign agents from multiple departments.

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

⚙️ Step 5: Allow Ticket Creation for All Users

- Navigate to: **Admin Panel → Settings → User Settings**
  - 🔲 Uncheck: Require registration and login to create tickets

✅ This allows unregistered users to submit tickets through the public form.

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

👩‍💻 Step 6: Add Agents (Staff Members)

- Navigate to: **Admin Panel → Agents → Add New**

- Example Agents:
	- Jane (Department: SysAdmins)
  - John (Department: Support)

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

👨‍👩‍👧 Step 7: Add Users (Customers)

- Navigate to: **Agent Panel → Users → Add New**

- Example Users:
  - Karen
  - Ken

🗣️ These are the end users who will submit tickets to the system.

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
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>

❓ Step 9: Create Help Topics

- Navigate to: **Admin Panel → Manage → Help Topics**
  
- Suggested Topics:
  - Business Critical Outage
  - Personal Computer Issues
  - Equipment Request
  - Password Reset
  - Other

🧾 Help Topics guide users to categorize their tickets properly.

</p>
<br />
