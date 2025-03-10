<p align="center">
<img src="https://github.com/user-attachments/assets/b700cc07-8ba1-4bfb-bd9c-c207d780fc10" height="50%" width="50%"/>
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
On the domain controller PC on the C:\drive, create 4 folders: “read-access”, “write-access”, “no-access”, “accounting”
</p> 
<p>
<img src="https://github.com/user-attachments/assets/c99439c7-950f-479f-bdde-a11004418641" height="80%" width="80%" /> 
</p>
<br />






























**Attempt to access file shares as a normal user**















**Create an "ACCOUNTANTS" Security Group, assign permissions, and test access**


















































