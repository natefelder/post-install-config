<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket -  Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source helpdesk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure
- Virtual Machine
- osTicket 


<h2>Good Things to Know</h2>

 - Links provided for better understanding of each topic
 	- [Roles](https://docs.osticket.com/en/latest/Admin/Agents/Roles.html)
	- [Departments](https://docs.osticket.com/en/latest/Admin/Agents/Departments.html)
	- [Teams](https://docs.osticket.com/en/latest/Admin/Agents/Teams.html) 
	- [Agents](https://docs.osticket.com/en/latest/Admin/Agents/Agents.html)
	- [Users](https://docs.osticket.com/en/latest/Agent/Users/User%20Directory.html).
	- [Service Level Agreement(SLA)](https://docs.osticket.com/en/latest/Admin/Manage/SLA%20Plans.html)
	
   

<h2>Installation Steps</h2>

<h3>Step 1: Open osTicket and Log In

1. Log in to osTicket using the credentials you made during the installation tutorial </h3>
	- If you need help or haven't installed osTicket, view my tutorial [here]
(https://github.com/natefelder/ostickets-prereqs)	

<p align="center">
<img src="https://i.imgur.com/gAXVBO2.png" height="80%" width="80%" alt="Azure Free Account"/>	


<h3>Step 2: Configure Roles </h3>

1. Make sure you are in the Admin panel (check the top-right of the screen to see which panel you are in)
	- If it says "Agent," you are in the Admin panel
2. Select the Agent tab > Roles > Add New Role
	- Name: Supreme Admin
	- Select Permissions tab and check every box under the "Tickets," "Tasks," and "Knowledgebase" sections
3. Select Add Role
	
<p align="center">
<img src="https://i.imgur.com/9tiOON2.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/CfCzRRk.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>


<h3>Step 3: Configure Departments</h3>

1. Ensure you are still in the Admin panel
2. Select the Agent tab > Departments > Add New Department 
	- Name: System Administrators
3. Select Create Department 


<p align="center">
<img src="https://i.imgur.com/f2uEloL.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/X2dXwjY.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>


<h3>Step 4: Configure Teams
</h3>

1. Select the Agent tab > Teams > Add New Team
	- Name: Level II Support 
2. Go to the Members tab and select yourself in "Select Agent" dropdown menu
- Select Create Team
	
<p align="center">
<img src="https://i.imgur.com/v6zzN3N.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/4IieS80.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>

<h3>Step 5: Allow Anyone to Create Tickets</h3>

1. Select Settings > User Settings
	- Make sure the following box is unchecked: 
		- Registration Required: Require registration and login to create tickets 
		
<p align="center">
<img src="https://i.imgur.com/kcd1jRf.png" height="80%" width="80%" alt="Azure Free Account"/>		


<h3>Step 6: Configure Agents</h3>

1. Select the Agent tab > Add New Agents
	- Name: Jane Doe
	- Email : jane.doe(@)osticket.com
	- Username: jane.doe
	- Click Set Password and uncheck the box that says "Send the Agent a Password Reset Email"
		- Set your password to anything you like
		- Uncheck the box that says "Require Password Change at Next Login"
		- Select set
		
<p align="center">
<img src="https://i.imgur.com/fTvI0Ru.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/6OU5KqX.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>

1. Select the Access tab 
	- Under Primary Department: 
		- Select the Department dropdown menu > System Administrators
		- Select the Role dropdown menu > Supreme Admin
	- Extended Accesss 
		- Select Department > Support > Add > Supreme Admin
2. Select Team tab
	- Select Team dropdown menu > Level II Support
	- Select Add
3. Select Create	

	
<p align="center">
<img src="https://i.imgur.com/HPSPHNU.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/hotx1wo.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>

1. Create another agent and replace Jane with John.
	- Follow the same steps as above, except make some changes to the Primary Department
		- Select the Department dropdown menu > Support
		- Select the Role dropdown menu > View Only
	- Extended Accesss 
		- Select Department > Support > Save Changes
		
<p align="center">
<img src="https://i.imgur.com/qQ8ckBr.png" height="70%" width="70%" alt="Azure Free Account"/> <img src="https://i.imgur.com/KVPsUb4.png" height="70%" width="70%" alt="Azure Free Services"/>
</p>
 
     

<h3>Step 7: Configure Users
</h3>

<p align="center">
<img src="https://i.imgur.com/UUqCK1d.png" height="80%" width="80%" alt="Azure Free Account"/>		
	
1. Select the Users tab to create a user
	- Email Address: Karen(@)osticket.com
	- Full Name: Karen Karen
	- Select Add User
	
<p align="center">
<img src="https://i.imgur.com/wpTn12W.png" height="80%" width="80%" alt="Azure Free Account"/>			
	
 1. Select the User tab again to create another user
	- Email Address: Ken(@)osticket.com
	- Full Name: Ken Ken
	- Select Add User

<p align="center">
<img src="https://i.imgur.com/EXyy5Gq.png" height="80%" width="80%" alt="Azure Free Account"/>		

<h3>Step 8:  Configure Service Level Agreements (SLA)
</h3>

1. We'll create three SLAs
2. Select the Manage tab > SLA > Add New SLA Plan

	- Name: SEV-A 			
	- Grace Period: 1
	- Schedule dropdown menu: 24/7
	- Select Add Plan
	
<p align="center">
<img src="https://i.imgur.com/fMR4yMR.png" height="80%" width="80%" alt="Azure Free Account"/> <img src="https://i.imgur.com/3tQnihq.png" height="80%" width="80%" alt="Azure Free Services"/>
</p>

	- Name: SEV-B
	- Grace Period: 4
	- Schedule dropdown menu: 24/7
	- Select Add Plan
	
<p align="center">
<img src="https://i.imgur.com/pAbQPEP.png" height="80%" width="80%" alt="Azure Free Account"/>

	- Name: SEV-C 
	- Grace Period: 8
	- Schedule dropdown menu: Monday - Friday 8AM - 5PM with U.S. Holidays
	- Select Add Plan

<p align="center">
<img src="https://i.imgur.com/5cgn0oz.png" height="80%" width="80%" alt="Azure Free Account"/>



<h3>Step 9:   Configure Help Topics
</h3>

- Configure Help Topics
  Help Topics will streamline your end-user’s help desk experience to ensure proper assignment   and prompt response to tickets. Create as many Help Topics as needed and can even add sub     categories to Help Topics within each other for further breakdown (Example, Human Resources   and Human Resources/Payroll.)
     <h5>Admin Panel -> Manage -> Help Topics<h5/>
        <li> Business Critical Outage </li>
        <li> Personal Computer Issues </li>
        <li> Equipment Request </li>
        <li> Password Reset </li>
  <p align="center">
    <img src="https://i.imgur.com/n44Un1L.png" height="65%" width="65%" alt="create new help topic"/>
</p>
    <p align="center">
    <img src="https://i.imgur.com/MOE3unk.png" height="65%" width="65%" alt="business critical outage"/>
    </p>
    <p align="center">
    <img src="https://i.imgur.com/6dBcOCd.png" height="65%" width="65%" alt="personal computer issue"/>
    </p>
    <p>Below selected items, reflect all of the tickets that we've created. The other tickets were created by default. </p>
<p align="center">
    <img src="https://i.imgur.com/RFC1bTH.png" height="65%" width="65%" alt="all tickets that have been created"/>
</p>
<p align="center"><b><i>You have configured osTicket</b></i></p>
<p align="center"><b><i>“Congratulations, this concludes this lab."</p></b></i>
<br />
<p align="right"> Next up, <a href="https://github.com/natefelder/ticket-lifecycle"
>Ticket Lifecycle </a></p>
