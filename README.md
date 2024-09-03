![image](https://github.com/user-attachments/assets/5983dcc7-4677-4a41-9945-fb88fe1003b1)![Screenshot 2024-09-03 141305](https://github.com/user-attachments/assets/4ed51a5d-b5e4-4f57-b373-0e0b9c0b7062)# Installing Active Directory on Windows Server 2022

We will continue building on our Active Directory lab by installing Active Directory onto our Windows Server 2022 VirtualBox VM! We will also do two other housekeeping tasks to make things run a bit smoother.

If you have not, please follow the initial steps to install VirtualBox and setup your Windows Server 2022 Virtual Machine!  

[Installing VirtualBox and Windows Server 2022](https://github.com/andrewkhun/virtualbox)

## Renaming your Server

The first thing we will do is rename our Windows Server. When we first created this server a name was automatically given to the machine, however this name is very difficult to remember and may give you issues when referencing it in later labs. Let's rename it to make it a bit easier to remember.

Right-click the start menu and select the Settings. Once inside the settings, scroll down until you see "Rename this PC (advanced)" and click that.

<img src="https://i.imgur.com/smPM6w6.png" height="70%" width="70%" alt="VirtualBox downloads"/>

The System Properties will open and an option to rename the computer will be available, click "Change". As you can see the initial name of our machine is very difficult to remember if we ever need to reference it in the future, so let's name it "Server2022". Click OK on the open windows to apply and your VM will restart to apply the changes.

<img src="https://i.imgur.com/5keQRPs.png" height="70%" width="70%" alt="VirtualBox downloads"/>

<img src="https://i.imgur.com/9ZvnQ4e.png" height="70%" width="70%" alt="VirtualBox downloads"/>

After restarting your VM will be successfully renamed.

## Enhancing Performance

The next task we can do is enhance our performance. Navigate to the settings menu once again and scroll down to the same area where we renamed our PC. Click on "Advanced System Settings" then click "Settings" under the Performance option. A window will pop up with options to adjust the Visual Effects of your machine. Select the option for "Adjust for Best Performance" and click OK on the windows to apply.

<img src="https://i.imgur.com/1wDsaU4.png" height="70%" width="70%" alt="VirtualBox downloads"/>

This will give a slight performance boost to our PC and make things run a little bit faster. 

Now we are ready to install Active Directory!

## Installing Active Directory

Open up Server Manager if it has not already been opened. On the top right select "Manage", then "Add Roles and Features" to get started.

<img src="https://i.imgur.com/9YHGLL5.png" height="70%" width="70%" alt="VirtualBox downloads"/>

<img src="https://i.imgur.com/Ut6KaeV.png" height="30%" width="30%" alt="VirtualBox downloads"/>

We will be adding a "Role-based or feature-based installation" as our Installation Type. 

<img src="https://i.imgur.com/1uTkqb9.png" height="70%" width="70%" alt="VirtualBox downloads"/>

For Server Selection, make sure our Server2022 is selected and click Next.

<img src="https://i.imgur.com/aHcQViy.png" height="70%" width="70%" alt="VirtualBox downloads"/>

For Server Roles, we will be selecting "Active Directory Domain Services". Make sure to check off the correct box. A window will appear that list the features we will be adding, click on "Add Features", then Next to continue.

<img src="https://i.imgur.com/nlJavSa.png" height="70%" width="70%" alt="VirtualBox downloads"/>

<img src="https://i.imgur.com/0MtYFTN.png" height="70%" width="70%" alt="VirtualBox downloads"/>

For Features and AD DS, click on Next to continue for both sections.

<img src="https://i.imgur.com/k9kUAHz.png" height="70%" width="70%" alt="VirtualBox downloads"/>

<img src="https://i.imgur.com/B3QFOxL.png" height="70%" width="70%" alt="VirtualBox downloads"/>

Once on the Confirmation page, click "Install" to begin the installation process.

<img src="https://i.imgur.com/qpvqG0i.png" height="70%" width="70%" alt="VirtualBox downloads"/>


## Promoting the Server to a Domain Controller

Once the installation process has completed, do NOT close the window just yet. Instead click on "Promote this server to a domain controller".

<img src="https://i.imgur.com/N56dpRK.png" height="70%" width="70%" alt="VirtualBox downloads"/>

Promoting a server to a domain controller allows it to manage and authenticate users, computers, and other resources within a network domain. It acts as the central authority for network security, ensuring that users have the right access to resources and enforcing security policies. In simple terms, it helps organize and control network resources efficiently and securely.

Select "Add a new forest" and create a name for your "Root domain name", for this lab we will simply name it "mydomain.com". Hit Next when ready. 

<img src="https://i.imgur.com/2x2I3d0.png" height="70%" width="70%" alt="VirtualBox downloads"/>

On "Domain Controller Options", create a password and make sure to remember it! Click Next when ready.

<img src="https://i.imgur.com/hCg9zKl.png" height="70%" width="70%" alt="VirtualBox downloads"/>

Leave "Create DNS delegation" unselected.

<img src="https://i.imgur.com/VLyXeSL.png" height="70%" width="70%" alt="VirtualBox downloads"/>

Click next for NetBIOS domain name as it should be auto-populated with our domain name. Continue to click Next, until the Install button is ready to be selected. Then click Install.

<img src="https://i.imgur.com/0qnY9bl.png" height="70%" width="70%" alt="VirtualBox downloads"/>

<img src="https://i.imgur.com/senZpIJ.png" height="70%" width="70%" alt="VirtualBox downloads"/>

<img src="https://i.imgur.com/RuPcMIk.png" height="70%" width="70%" alt="VirtualBox downloads"/>

<img src="https://i.imgur.com/VhPWjFw.png" height="70%" width="70%" alt="VirtualBox downloads"/>

Once finished installing, the computer will restart.

<img src="https://i.imgur.com/G97A2l6.png" height="30%" width="30%" alt="VirtualBox downloads"/>

Once restarted, log back in and head over to the Windows Server Manager once again. Click on "Tools" and select "Active Directory Users and Computers".

<img src="https://i.imgur.com/RygVEkE.png" height="30%" width="30%" alt="VirtualBox downloads"/>

<img src="https://i.imgur.com/EZQTHeF.png" height="70%" width="70%" alt="VirtualBox downloads"/>





