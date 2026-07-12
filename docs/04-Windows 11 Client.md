Step 1: Create Windows 11 VM
-------------------------------
VirtualBox Settings:
  - Name: Client01
  - Ram: 6060
  - CPU: 2
  - Disk: 64 gb
  - Adapter 1: NAT
  - Adapter 2: Internal Network: homelab

<img width="489" height="523" alt="image" src="https://github.com/user-attachments/assets/e2ce82ce-6674-478f-83b0-3655410f26d4" />

Step 2: Set Static Ip on Client
---------------------------------
1. On Windows 11, set the internal network adapter:
      - IP Address: 192.168.10.100
      - Subnet Mask: 255.255.255.0
      - DNS Server: 192.168.10.10
- the DNS point to the domain controller
<img width="1024" height="768" alt="ip v4 client settings" src="https://github.com/user-attachments/assets/abeedbe9-1ae0-43ff-9175-0393994a8886" />

Step 3: Connect Windows 11 to Domain
-------------------------------------
1. Go to Settings
2. Then System
3. About
4. Find Domain or Workgroup
5. Click Change
6. Select Domain
7. Type in helpdesk.local to join that domain
<img width="1024" height="768" alt="join domain client vm" src="https://github.com/user-attachments/assets/8a2afb2b-02ba-403b-b183-b22ae383e64c" />

8. Then Enter into Computer/Domain Changes using Administrator@helpdesk.local as username and password from server vm Helpdesk123!
<img width="915" height="726" alt="image" src="https://github.com/user-attachments/assets/8af49c41-3354-45a4-8d34-e991986665d1" />

10. Client vm Successfully joins domain
<img width="1024" height="768" alt="client vm joined domain" src="https://github.com/user-attachments/assets/72b3c8dc-3c05-458f-b844-770c286f969f" />

Step 4: Log into as Domain User(Client)
-----------------------------------------
1. At Login Screen, Choose other user in the bottom left of screen
2. Login as helpdesk\jsmith, Use the email Jsmith@helpdesk.local and Password: Password123! (Note that it will prompt password change after first login)
<img width="1024" height="768" alt="domain user login on client" src="https://github.com/user-attachments/assets/62656b94-7e66-49dc-8588-7f982f5070a6" />
