# Implementing_Active_Directory
## Descripton
Project consists of showing user how to implement Active dierctory.
Active Dierctory is a core of managing any team, and allows for Identity managemnt, User authentication, Group policys and more. 

Envirmonts used: Azure, WIndows 10, WIndows server, Virtual machines

Azure Subscription: You'll need an active Azure subscription.
### Steps
Create two VMs, one being a windows server and the other a windows 10 Vm.Make sure to put your Server and your Windows 10 Vm on the same Resouce group and in the same regin to not cause problems.
![jEYjm1txUm](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/460fc7ee-d72c-41ff-847e-0f17004da97c)
This is my Windows Vm you can see the settings i have like what version of windows and what vm specs/size i used. I named mine Client-1 you can name your anyhting you would like. 
![VJgXOsx9RS](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/33372909-6a24-43c2-8141-b373e5de0358)
This is my Windows server Vm you can agian see settings and specs i used. I named mine Dc-1 test you can name yours anything that you would like. 
![cg06Re9rcy](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/8b238967-970d-4d9c-a5fb-a0a3cf2aca13)
 We will also make sure to make that our server is set to a static ip address.
![veucaY92JW](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/7970d69b-12ed-4dda-b83f-ab898a7aee67)
 Next we will log into our Windows Server and Install Active Directory. select "add roles and features"
![DZqubc60fs](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/b4e975a3-49bf-482f-a96a-a2c287578e54)
We will be hitting next on these screens. (hit next three more time)
![3BSO33Qxq0](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/e2ec20b1-b7a5-480b-95a8-0a9ed7d450f8)
![3IVQzEANBl](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/87036e00-8c6d-4f8a-a3ca-1dbed60b414a)
![VRoEW9M8UO](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/dc6965c5-6a13-4d81-8405-05d9d5a5fe36)

When on "Server Roles" Select "Active Directory Domain Services" and select next. 
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

From this screen you will select "add a new forest", for Root domain name you can name it anything but it has to have a .com like a website. I will be using Testing.com for mine. and select "next

![xaQDJbjyk5](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/ab98067e-570a-4bf7-97bd-86a3e86cb268)

Here you will create a password and select "next"

![MBMY8dvZFr](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/a62ddfb1-2ce4-45dc-a355-c127f50e28c3)

Contuinue to select "next" until you rach this page and select "install". This will take a minuite and it will also restart your Remote desktop sestion. When done reconnect to WIndows Server 

![MKpT9j9Xci](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/7073c9dc-e857-477a-83cd-56f2f0d865cc)

Open back up your windows server vm, and open "Sever manager". Select "tools and select "Active Directory Users and Computers"

![SgQpgmzS6t](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/31a0f71c-f2ff-40e9-8e9f-143c273ad906)

Then select what domain name you entered.(mine being Testing.com) Right-click and hover over new and select "Organizational untit", We will be make two one named _EMPLOYEES and _ADMINS.

![uDlY91815a](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/0f63f52d-f85c-4186-84e7-4466b05865fd)
![ajBzoTYMDD](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/717d1096-d0a1-40a5-9d59-8d47ebc13e99)
![PppQIUh6gP](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/4e39bab4-8765-4d1d-bcf8-bab25923ac9b)

To add admins go to the file you created called _ADMINS. Right-click and hover over new and select "User"
![dXuRO2717X](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/efa8977b-576a-4a34-9737-be094da04211)

You will see this pop-up window fill it in but for this example i will be using John Doe. Then select "next"

![AKSmEZzubJ](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/aecaf9a8-be78-45fc-969d-4c8e7d4c9ed9)
![uTeXOQMd2A](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/04b27f62-d2ba-48be-99fe-727b6dbe0593)

Here you can set their one time password and change password settings and if you would want the user to change their passowrd when they first log-in. 

![mfTOYnoMiS](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/b14a063a-3f9f-4eba-a0b3-16cd4cf79801)
![kDWENf6Qfn](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/c5d0b93c-8f02-45e3-8da9-479d68d9ef21)

Now we need to asgian the Domain admin group to the admin we just made. Right-click the user you made and select "Properties" 

![23aXaLvMsU](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/225f6f52-2ff6-48b5-9d2b-353d2dac13c1)

Then select "Member of"

![cJbNCzW8zs](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/b2689074-d7c3-459a-a06d-e057692212a3)

You will select Add, in the box enter "domain" and select "Check names" and select "Domain Admins"














Validate that your Azure-based Active Directory is operational by creating users, groups, and objects.
Ensure that your on-premises Active Directory can communicate with the Azure VM.
Backup and Maintenance:


Implement best practices for maintaining AD DS, such as monitoring, patching, and disaster recovery planning.
Integrate with On-Premises AD (Optional):
