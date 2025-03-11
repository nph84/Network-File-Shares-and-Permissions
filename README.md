<p align="center">
<img src="https://github.com/user-attachments/assets/a03fa6e8-a8c7-4562-9bc7-c086861405f2" height="40%" width="40%"/>
</p>

<h1>Network File Shares and Permissions</h1>
This tutorial outlines the steps required to change access permissions to network file shares.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create some sample file shares with various permissions
- Attempt to access file shares as a normal user
- Create an "ACCOUNTANTS" Security Group, assign permissions, and test access

<h2>Deployment and Configuration Steps</h2>

**Create some sample file shares with various permissions**
<p>
Log in to the domain controller PC as an administrator.
</p> 
<p>
<img src="https://github.com/user-attachments/assets/d8b104a2-39b5-482e-9fcb-c438b1a17c65" height="80%" width="80%" /> 
</p>
<br />


<p>
Log in to the client PC as a normal user.
</p> 
<p>
<img src="https://github.com/user-attachments/assets/d86b619f-5499-4aa0-b18a-bfb979186a67" height="80%" width="80%" /> 
</p>
<br />




<p>
On the domain controller PC on the C:\drive, create 4 folders: “read-access”, “write-access”, “no-access”, “accounting”.
</p> 
<p>
<img src="https://github.com/user-attachments/assets/c99439c7-950f-479f-bdde-a11004418641" height="80%" width="80%" /> 
</p>
<br />




<p>
Set the following permissions (share the folder)
a.	Folder: “read-access”, Group: “Domain Users”, Permission: “Read”
b.	Folder: “write-access”,  Group: “Domain Users”, Permissions: “Read/Write”
c.	Folder: “no-access”, Group: “Domain Admins”, “Permissions: “Read/Write”
d.	(Skip accounting for now)
</p> 
<p>
<img src="https://github.com/user-attachments/assets/72e79bda-210c-4e92-aa5c-b7a0e4f58c4e" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/3a4e825a-256d-4f38-adb7-bea738ae6e9b" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/f0167133-466d-4a59-bbbe-4c463d5059ca" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/373464e6-7623-4b2d-a2e0-0888dfa7f0d1" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/bb5cd244-9b2b-4da2-a48a-a741011f018c" height="80%" width="80%" />
 <br />

Repeat these steps for the subsequent groups, setting the appropriate file permissions.
</p>
<br />




**Attempt to access file shares as a normal user**


<p>
On client PC navigate to the shared folder.
</p> 
<p>
<img src="https://github.com/user-attachments/assets/3e97d621-7056-45ba-b72d-1213f8295c6a" height="80%" width="80%" /> 
</p>
<br />




<p>
Try to access the folders you just created. Which folders can you access? Which folders can you create stuff in? Does it make sense?
</p> 
<p>
<img src="https://github.com/user-attachments/assets/3e97d621-7056-45ba-b72d-1213f8295c6a" height="80%" width="80%" /> 
</p>
<br />




**Create an "ACCOUNTANTS" Security Group, assign permissions, and test access**

<p>
Go back to the domain controller. In Active Directory, create a new organizational unit called "_GROUPS". Inside this new group, create a security group called “ACCOUNTANTS”
</p> 
<p>
<img src="https://github.com/user-attachments/assets/15df9cac-93af-4f27-a3b9-8278f5ea67d7" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/ada366b1-f275-48c4-84a6-1086941ef5e3" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/35d490b5-bc11-42ad-a6d8-44d6a40af6d1" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/578ce676-f164-4a81-90f6-424486e2cea1" height="80%" width="80%" />
</p>
<br />














































