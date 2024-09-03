# Installing Active Directory on Windows Server 2022

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

