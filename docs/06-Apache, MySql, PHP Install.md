Step 1: On Ubuntu
-----------------------
1. Commands for Ubuntu: sudo apt update && sudo apt upgrade -y
2. Install Apache:
     - sudo apt install apache2 -y
     - sudo systemct1 status apache2
3. Install MySql:
     - sudo apt install mysql-server -y
     - sudo mysql_secure_installation
     - MySql Settings:
           - Validate password components: N
           - Remove anonymous users: Y
           - Disallow  root login remotely: Y
           - Remove test database: Y
           - Reload privilege tables: Y
   
