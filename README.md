 # Implementing_Active_Directory
## Description
Project consists of showing users how to implement Active directory.
Active Directory is a core of managing any team and allows for Identity management, User authentication, Group policies, and more. 

Environments used: Azure, WIndows 10, WIndows server, Virtual machines

Azure Subscription: You'll need an active Azure subscription.
### Steps
Create two VMs, one being a Windows server and the other a windows 10 VM. Make sure to put your Server and your Windows 10 VM on the same Resouce group and in the same region to not cause problems.
![jEYjm1txUm](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/460fc7ee-d72c-41ff-847e-0f17004da97c)
This is my Windows VM you can see the settings I have like what version of Windows and what VM specs/size I used. I named mine Client-1 you can name anything you would like. 
![cg06Re9rcy](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/8b238967-970d-4d9c-a5fb-a0a3cf2aca13)
 We will also make sure to make sure that our server is set to a static IP address.
![veucaY92JW](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/7970d69b-12ed-4dda-b83f-ab898a7aee67)
 Next, we will log into our Windows Server and Install Active Directory. select "add roles and features"
![DZqubc60fs](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/b4e975a3-49bf-482f-a96a-a2c287578e54)
We will be hitting next on these screens. (Hit the next three more times)
![3BSO33Qxq0](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/e2ec20b1-b7a5-480b-95a8-0a9ed7d450f8)
![3IVQzEANBl](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/87036e00-8c6d-4f8a-a3ca-1dbed60b414a)
![VRoEW9M8UO](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/dc6965c5-6a13-4d81-8405-05d9d5a5fe36)

When on "Server Roles" Select "Active Directory Domain Services" and select Next. 
![kbXRZoRfwI](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/0dcf4ee0-867f-4010-bb1d-c50659695939)

Select "Next" two more times.

![xPRF4hoN2e](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/2da27593-5c5b-423b-a079-ecd317e3dfd1)
![6sTYoWGBb3](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/a8e78e7c-d555-4880-8abd-59e9e11f7899)

Select "install"

![OnLRqVdPuR](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/b81e46ad-869e-4c8b-a8f9-0bd3e5febb92)

Select "close"

![ckqva7oQLx](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/18a2ef89-902d-4fe1-b224-bc20ddccd420)

Select "Promote this server to a domain controller"
![WaIgeT2fvG](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/26a843f9-6103-4847-ac6d-367a98091b27)

From this screen, you will select "add a new forest", for the Root domain name you can name it anything but it has to have a .com-like website. I will be using Testing.com for mine. and select "next

![xaQDJbjyk5](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/ab98067e-570a-4bf7-97bd-86a3e86cb268)

Here you will create a password and select "next"

![MBMY8dvZFr](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/a62ddfb1-2ce4-45dc-a355-c127f50e28c3)

Continue to select "next" until you reach this page and select "install". This will take a minute and it will also restart your Remote desktop session. When done reconnect to Windows Server 

![MKpT9j9Xci](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/7073c9dc-e857-477a-83cd-56f2f0d865cc)

Open back up your Windows server VM, and open "Sever manager". Select "Tools and select "Active Directory Users and Computers"

![SgQpgmzS6t](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/31a0f71c-f2ff-40e9-8e9f-143c273ad906)

Then select what domain name you entered. (mine being Testing.com) Right-click and hover over new and select "Organizational unit", We will make two ones named _EMPLOYEES and _ADMINS.

![uDlY91815a](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/0f63f52d-f85c-4186-84e7-4466b05865fd)
![ajBzoTYMDD](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/717d1096-d0a1-40a5-9d59-8d47ebc13e99)
![PppQIUh6gP](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/4e39bab4-8765-4d1d-bcf8-bab25923ac9b)

To add admins go to the file you created called _ADMINS. Right-click and hover over new and select "User"
![dXuRO2717X](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/efa8977b-576a-4a34-9737-be094da04211)

You will see this pop-up window fill it in but for this example, I will be using John Doe. Then select "next"

![AKSmEZzubJ](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/aecaf9a8-be78-45fc-969d-4c8e7d4c9ed9)
![uTeXOQMd2A](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/04b27f62-d2ba-48be-99fe-727b6dbe0593)

Here you can set their one-time password and change password settings if you would want the user to change their password when they first log in. 

![mfTOYnoMiS](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/b14a063a-3f9f-4eba-a0b3-16cd4cf79801)
![kDWENf6Qfn](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/c5d0b93c-8f02-45e3-8da9-479d68d9ef21)

Now we need to assign the Domain admin group to the admin we just made. Right-click the user you made and select "Properties" 

![23aXaLvMsU](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/225f6f52-2ff6-48b5-9d2b-353d2dac13c1)

Then select "Member of"

![cJbNCzW8zs](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/b2689074-d7c3-459a-a06d-e057692212a3)

You will select Add, in the box enter "domain" and select "Check names" and select "Domain Admins" Then select "Okay" and "Apply"

![liggpONZ6U](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/d6dd1c8b-e38f-42e9-be31-5c9a180714d1)
![XIks9A9Cw6](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/1d482281-0c93-4e29-b9f1-5ef0d49178c8)
![Fp5fK3Pxjk](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/17ed06a5-2d11-426a-b588-17b3cbb8d40f)

You should now be able to Log in as the Admin you just made, I suggest doing it just to make sure it works. Now we will join out Windows 10 Vm (CLient-1) to our server. go to settings then "About" find "Rename this PC" and select it. 
![XwS1VRRwfv](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/0d7bde0b-ebb5-4367-9992-319997167f96)

Then select "Change..." 

![vly0VQhVT5](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/4f54bac8-9ab8-480d-bd0d-b75f1bc8d81a)

Select "Domain" and type in your Domain. (Mine being Testing.com)

![HsuEq2G4sG](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/7a5897f0-ca05-42fb-bf50-7b4dc6a1aeb9)
![1ApDvzXNnF](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/fc7c024f-15d6-4d70-87c9-a318870efd54)

Now we are going to back into Azure and set WIndows 10 server (CLient-1) DNS settings to our Servers Private IP address. Go to your server on Azure and copy your Nic private IP, then go to your Windows 10 VM (client-1) select "Networking" and then "Network Interface".

![GSRkqBX2P3](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/33750dfc-3923-455a-9392-753ee267c139)

Select "DNS Servers" then select "Custom" enter in the server's private IP and select "Save"
![hC6LUN0rPt](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/69f4a925-128d-4de7-ac63-1a3e97a6a540)

Go ahead and restart your Windows 10 Vm (client-1). You are now set and can change and add new users as you need to. You are also able to change settings like who can access Remote Desktop and permissions. 

You have now successfully implemented Active Directory, Thank you for following this guide and please let me know if you have any issues.  
