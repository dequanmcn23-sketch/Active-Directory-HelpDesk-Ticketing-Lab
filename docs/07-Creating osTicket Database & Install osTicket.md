Part 7: Creating Database
Step 1: Open Sql
----
- This is a dedicated MySQL database and user were created for osTicket instead of using the root account.

Command: 
sudo mysql

Run:
---------
CREATE DATABASE osticket;

CREATE USER 'osticketuser'@'localhost' IDENTIFIED BY 'Password123!';

GRANT ALL PRIVILEGES ON osticket.* TO 'osticketuser'@'localhost';

FLUSH PRIVILEGES;

EXIT;

<img width="813" height="254" alt="mysql ubuntu" src="https://github.com/user-attachments/assets/ebff69b3-8659-4aa8-8029-282ad8080b21" />

Part 8: Install osTicket
--------------------------
1. Go to web directory:
   - cd /var/www/html

2. Download osTicket:
   - sudo git clone https://github.com/osTicket.git osTicket
  
3. Go into folder:
   - cd osTicket
5. Install dependencies/submodules:
   - sudo git submodule update --init --recursive
6. Copy Config file:
   - sudo cp include/ost-sampleconfig.php inlcude/ost-config.php
7. Set permissions:
   - sudo chown -R www-data:www-data /var/www/html/osticket
   - sudo chmod 0666 /var/www/html/osticket/include/ost-config.php
  
8. Restart Apache:
   - sudo systemct1 restart apache2

9. To Verify Open From Window 11 Client Browser: https://192.168.10.20/osTicket

<img width="1024" height="768" alt="complete osticket" src="https://github.com/user-attachments/assets/5c9a77ac-8bf1-4d13-b41d-e40b5313276a" />




