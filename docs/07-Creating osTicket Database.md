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
