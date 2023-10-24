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

From this screen you will select "add a new forest", for Root domain name you can name it anything but it has to have a .com like a website. I will be using Testing.com for mine. 

![WHrDt4vWuh](https://github.com/JustinTHewitt/Implementing_Active_Directory/assets/146316539/fe179932-f462-4bc8-afa4-320232a2f4a7)



After AD DS is installed, open "Server Manager."
Click on "Tools" and select "DNS" to open the DNS Manager.
Create a forward lookup zone for your domain if it doesn't exist.
Ensure that the DNS server points to itself as the primary DNS server (127.0.0.1) in its network settings.
Azure Network Configuration:

Ensure that your VM's network security group allows traffic on the necessary AD DS ports (TCP/UDP 389, TCP 636).
Set up appropriate NSG rules to allow communication between your on-premises network and Azure.
Replication:

If you have an on-premises Active Directory, you can configure replication between your on-premises domain controllers and the Azure VM. This typically involves setting up a VPN or Azure ExpressRoute for secure communication.
Testing:

Validate that your Azure-based Active Directory is operational by creating users, groups, and objects.
Ensure that your on-premises Active Directory can communicate with the Azure VM.
Backup and Maintenance:

Regularly back up your Azure VM running AD DS.
Implement best practices for maintaining AD DS, such as monitoring, patching, and disaster recovery planning.
Integrate with On-Premises AD (Optional):

If you have an existing on-premises AD, you can set up AD synchronization, Federation Services (AD FS), or Azure AD Connect to enable seamless authentication and user management between on-premises and Azure AD.
Remember to follow security best practices and consider high availability and redundancy options for your Azure-based Active Directory. This guide provides a high-level overview, and the actual implementation may vary depending on your specific requirements and existing infrastructure.
