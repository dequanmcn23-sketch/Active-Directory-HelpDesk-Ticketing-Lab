Step 1: Create Ubuntu VM
--------------------------
- Ubuntu Server is configured with a static ip address of 192.168.10.20 on the Helpdesklab interanl network.

VirtualBox Settings:
--
- Name: Ubuntu(osTicket)
- Type: Linux
- Ram: 4096
- CPU: 2 cores 
- Disk: 40 gb

- Create Account:
    - Username: helpdesk
    - Password: Password123!
    - Hostname: osticket
 
<img width="1280" height="800" alt="osticket login again" src="https://github.com/user-attachments/assets/4df46fb2-f19d-4a58-ac35-7e891ab0a905" />

Step 2: Configure Static IP 
---------------------------

1. Check Interfaces: ip -br addr
       - enp0s3 = NAT , enp0s8 = internal network: homelab

2. Edit netplan:
     - using this command:  sudo nano /etc/netplan/00-installer-config.yaml
     - configuring :
```yaml
network:
  version: 2
  renderer: networkd
  ethernets:
    enp0s3:
      dhcp4: true
      dhcp6: false

    enp0s8:
      dhcp4: false
      dhcp6: false
      addresses:
        - 192.168.10.20/24
      nameservers:
        addresses:
          - 192.168.10.10
        search:
          - helpdesk.local
```
3. Save:
    - CTRL + O, ENTER, CTRL + X

4.Check: Using ip -br addr

<img width="1280" height="800" alt="yaml and ip addr ubuntu" src="https://github.com/user-attachments/assets/f48dd87c-c094-4b71-82b4-9644664f2257" />

Step 3: Test Network 
---------------------

1. From Ubuntu using pings to test connection between client vm and DC01(Server) vm
   - ping 192.168.10.100 -client
<img width="1142" height="185" alt="ubuntu can communicate with client" src="https://github.com/user-attachments/assets/bd760b33-6f45-4bda-8942-82bfe03e16dd" />


   - Successful ping 192.168.10.10 -DC01
<img width="1136" height="178" alt="ubuntu talking with Server" src="https://github.com/user-attachments/assets/22b4a520-6d93-4f50-bf1d-e77a3e91d093" />

2. From Windows 11 Client to Ubuntu and Window Server 
    - ping 192.168.10.20
    - ping 192.168.10.10
      <img width="1024" height="768" alt="client communicates with ubuntu" src="https://github.com/user-attachments/assets/333bbdd4-e7b3-4c6e-896c-a2de2c2d6e4c" />

  
