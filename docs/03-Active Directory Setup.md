Active Directory Configuration 
--------------------------------
Part 1. Static Ip Configuration 
------------------------
1. Navigate to Control Panel
2. Click on Network and Internet
3. Next Network and Sharing Center
4. Click on Ethernet 2 because thats the adapter for the homelab domain
5. Next go to properties and find IPv4 and Click on properties and change the IP, Subnet and DNS to the following:

<img width="1024" height="768" alt="static ip config windowserver" src="https://github.com/user-attachments/assets/d534a8bd-cfa9-4573-8763-5fc7742bb9b3" />

Part 2: Install Active Directory 
--------------------------------

Step 1. Add AD DS Role
-----------------
1. Open Server manager
2. Manage
3. Add Roles and Features
4. Choose Role Based or feature Based Installation
5. Select DC01
6. Choose Active Directory Domain Services and Dns
7. Add Features and Install


<img width="1024" height="768" alt="ad ds install" src="https://github.com/user-attachments/assets/3c1eaa77-5ff4-4790-b7ad-2f44f3acb5b3" />

Step 2. Create a Domain 
--------------------
1. After Install Click the yellow flag in Server Manager
2. Click on Promote this server to a domain controller
3. Choose add a new forest
4. Domain Name: helpdesk.local
5. Set a DSRM Password
6. Continue through install process


<img width="1024" height="768" alt="promo dcm" src="https://github.com/user-attachments/assets/1a836a50-9afd-4ae6-aa73-bd2620fa88b5" />

Part 3: Create OUs, Users, and Groups
--------------------------------------
  - Purpose: Organizational Units were created to organize users, groups, computers, and departments.
1. Open Server Manager >> Tools >>> Active Directory Users and Computers
2. Expand helpdesk.local

Step 1: Create OUs
-------------------
1. Right Click Helpdesk.local
2. Choose New and Find Organizational Unit
3. Repeat this
4. Create OUs :
     - Users
     - Groups
     - Computers
     - Sales
     - IT
     - Managers
     - Helpdesk

<img width="1024" height="768" alt="ad ou structure" src="https://github.com/user-attachments/assets/2f365647-1d81-4763-b851-481e224eb0e5" />

Step 2: Create Security Groups
-------------------------------
 - Purpose: Security groups were created to simulate department-based permissions and help desk responsibilities.
1. Inside the Groups OU, Create:
2. For each Group: Group Scope: Global, Group Type: Security
    - Sales
    - IT-admins 
    - Managers 
    - Helpdesk-Team
    - Password-Reset-Tech

<img width="1024" height="768" alt="groups ou all security groups" src="https://github.com/user-attachments/assets/f575d687-0f31-4522-b5d5-18873268bffe" />

Step 3: Create Users
-----------------------
1. Create Users inside the Users OU first
2. Create:
      - Full Name	 - Username	- Department
      - John Smith	 - jsmith	- Sales
      - Sarah Jones	 - sjones - Managers
      - Mike Brown	 - mbrown	- IT
      - Alex Wilson	- awilson	  - HelpDesk
      - Robert Taylor	- rtaylor	- Sales
3. Use temp password
4. For Lab simplicity, check: Password never expires

<img width="1024" height="768" alt="creating users in user ou" src="https://github.com/user-attachments/assets/f18ea072-6f66-4441-b9f6-1d947cbee2d3" />

Step 4: Move Users to Department OUs 
--------------------------------------
- Purpose: Users were moved into department OUs to simulate a real company structure.
1. Move Users
2. Right click User: Move, Select Correct OU, Ok
   - Users          - Move to OU
   - jsmith         - Sales
   - rtaylor        - Sales
   - sjones         - Managers
   - mbrown         -  IT
   - awilson        - Helpdesk

<img width="1024" height="768" alt="sales ou with users" src="https://github.com/user-attachments/assets/625a92c7-23ad-4e73-a98c-1247626665f3" />
<img width="1024" height="768" alt="it ou wit users" src="https://github.com/user-attachments/assets/4e6894ab-0c29-47fb-9886-584fc7d93209" />
<img width="1024" height="768" alt="manager ou users" src="https://github.com/user-attachments/assets/3fedb99d-6ae7-4269-bb01-7fa0c2257571" />
<img width="1024" height="768" alt="helpd ou users" src="https://github.com/user-attachments/assets/4d61ba9f-e3e3-4950-bf8e-34fcc5e653b8" />

Step 5: Add Users to Security Groups
--------------------------------------
1. Add Users to Groups
2. To add a user to a group : Double click user, Member of, Add, Type group name, check names, ok , and apply

   - Users    -Group
   - jsmith   - Sales
   - rtaylor  - Sales
   - sjones   - Managers
   - mbrown   - It-Admins
   - awilson  - Helpdesk-Team
   - awilson  - Password-Reset-Tech
  
  

<img width="1024" height="768" alt="wilson in groups" src="https://github.com/user-attachments/assets/0968611d-cd76-4a1d-9ec9-783a9e30825b" />
<img width="1024" height="768" alt="brown in groups" src="https://github.com/user-attachments/assets/efcb6af4-2ea7-4d0d-bba7-daf7b9cdfe86" />






















