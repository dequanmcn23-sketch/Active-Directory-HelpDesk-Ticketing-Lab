Step 1: On Ubuntu
-----------------------
1. Commands for Ubuntu: sudo apt update && sudo apt upgrade -y
2. Install Apache:
     - sudo apt install apache2 -y
     - sudo systemct1 status apache2
  <img width="672" height="80" alt="apache installed" src="https://github.com/user-attachments/assets/ce540ccc-9105-4a72-9a23-b080c3938d43" />

3. Install MySql:
     - sudo apt install mysql-server -y
     - sudo mysql_secure_installation
     - MySql Settings:
       - Validate password components: N
       - Remove anonymous users: Y
       - Disallow  root login remotely: Y
       - Remove test database: Y
       - Reload privilege tables: Y
      
4. Install PHP:
     - sudo apt install php php-mysql php-gd php-imap php-curl php-xml php-mbstring php-intl php-apcu unzip git -y
<img width="1020" height="111" alt="php installed" src="https://github.com/user-attachments/assets/713d9780-60f8-486c-a2c4-b3e54633cd13" />

5. Restart Apache:
        - sudo systemct1 restart apache2
