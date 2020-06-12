# Create Host Pool from Azure Portal 
# Create Host Pool from Azure Portal 
 
 Host pools are a collection of one or more identical virtual machines within Windows Virtual Desktop environments. Each host pool can contain an app group that users can interact with as they would on a physical desktop. 

1. Login to the Azure portal using the credentials in the Lab Environments section. 

2. In the search bar, search for ‘Windows Virtual Desktop” and you will see a resource that shows up in the same name. Click on it. 

![ws name.](media/1.png)
 

3. You will be directed towards the Windows Virtual Desktop(Hereafter referred as WVD) management window.  

![ws name.](media/2.png)


4. In the management tab, select **Host pools**. 

![ws name.](media/3.png)


5. Click on Add to add new Host Pool. 

![ws name.](media/4.png)


6. Creating a Host Pool is divided into multiple sections. The first one is the Basic section. All the fields in this section are explained below along with the values: 

 ![ws name.](media/5.png)
 
 
**A.** Project Details – Defines the environment 

**Subscription**: Choose the default subscription

**Resource Group**: Choose the default pre-created Resource Group

**Host Pool Name**: WVD-HP-01 

**Location**: Choose the location of the pre-created resource Group

**B.** Host Pool Type – Defines the type of host pool. 

1. **Host pool type**: Pooled
 

       Host Pools are of 2 types:
       1.	Pooled
       2.	Personal
       Pooled is used to share the same Session Host (Virtual Machine) resources among multiple users, while Personal uses a dedicated   Session host of individual user.

   
    

    
2. **Max session Limit**: 5


       Max session Limit limits the simultaneous number of users on the same session host.
  
    
   
3. **Load Balancing Algorithm**: Breadth First



       Load Balancing Algorithm are of 2 types:
       1. Breadth-first
       2. Depth-first

       Breadth-first load balancing distributes new user sessions across all available session hosts in the host pool. Depth-first load balancing distributes new user sessions to an available session host with the highest number of connections but has not reached its maximum session limit threshold.
   
   

   
7. In the Virtual machines tab, select **Yes** against **Add virtual machines**. By doing this, we are stepping towards adding Virtual machines to the host pool. 

![ws name.](media/9.png)

8. Now a long list of parameter appears. These can be categorized into three: Session Host specifications, Network and Security, Domain and Administrator account. 

  A. Session Host Specifications 

   In this section, we provide the details of the VMs to be created as session Hosts. 
   
   ![ws name.](media/10.png)
   

   **Resource Group**: Choose the default pre-created Resource Group

   **Virtual machine location**: Choose the location of the pre-created resource Group

   **Virtual machine size**: Standard D1_V2 

   **Number of VMs**: 2 
   
   **Name prefix**: WVD-SH 

   **Image type**: Gallery 

   **Image**: Windows 10 Enterprise multi-session, version 1909 + Office 365 ProPlus (choose from dropdown) 

   **OS disk type**: Standard SSD 

   **Use managed disks**: Yes 
   
   
  B. Network and Security 
 
   ![ws name.](media/11.png)
   
  
  **Virtual Network**: Default value

  **Subnet**: Default value

  **Public IP**: Default value

  **Network security Group**: Default value

  **Public inbound ports**: Default value
 
 
 c. Domain and Administrator account 

  ![ws name.](media/12.png)
 

   **Specify Domain or Unit**: No 

   **AD domain join UPN**: Provide the username from ‘Lab Environment’ Tab

   **Password**: Provide the password from the ‘Lab Environment’ Tab

   **Confirm Password**: Confirm the password from the ‘Lab Environment’ Tab
   
9. Click on Next:Workspace to proceed. 

10. In the Workspace section, we need to specify if we need to register the default application group with a workspace. 

    ![ws name.](media/13.png)
    
    
**Register desktop app group:** Yes 

**To this workspace:** Create new
    
11.  Once you click the **Create new**, a small window pops up, where you can specify the Workspace name you are going to create.  

![ws name.](media/14.png)


**Workspace name:** WVD-WS-01 
Click **OK** 

12. Once we fill up all the parameters, click on the  **Review + create** button on the bottom left corner. 

![ws name.](media/15.png)


13. The last window helps us verify if the parameters we filled are correct. If yes, click on Create to initiate the deployment. 

![ws name.](media/16.png)


14. The deployment starts, wait until the deployment gets succeeded.  

![ws name.](media/17.png)


![ws name.](media/18.png)
 
 
Click on **Go to Resource**.

15. You will see that the **Hostpool WVD-HP-01** is created with 2 session hosts in it, and a default application group (of type Desktop). 

Click on **Session Hosts** 

![ws name.](media/19.png)


16. Notice the Session Hosts created, with a name concatenating the Name Prefix and increment number. 


![ws name.](media/20.png)

