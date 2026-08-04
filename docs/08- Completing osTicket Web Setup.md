Settings:

- osTicket was installed on Ubuntu Server and connected to a Mysql database
-----------
Use:
  - Helpdesk Name: Home Helpdesk
  - Default Email: admin@helpdesk.local
  - Admin Username: admin
  - Admin Password: Password123!


Database Settings:
-------------------
Use: 
  - Mysql Hostname: localhost
  - Database: osticket
  - Username: osticketuser
  - Password: Password123!
<img width="1024" height="768" alt="osticket setup page complete" src="https://github.com/user-attachments/assets/b9ced385-ef96-4809-b5fd-8ed1c1b92776" />

After Install:
----------------
Run command:
  - sudo rm -rf /var/www/html/osticket/setup
  - sudo chmod 0644 /var/www/html/osticket/include/ost-config.php
