Objective

Create a fully functional virtual IT Help Desk environment capable of managing users, supporting a Windows domain, and handling help desk tickets.

Lab Environment
Machine	Role
Windows Server	Domain Controller
Ubuntu Server	osTicket Server
Windows 11	Client Workstation
Network Layout
Internet
     │
VirtualBox NAT
     │

Internal Network
HelpDeskLab

     │
 ├──────────────┐
 │              │
DC01       OSTICKET
 │              │
 └────CLIENT01──┘
