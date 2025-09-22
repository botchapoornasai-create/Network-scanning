# Network-scanning
#Nmap

DEF-network scanning is the process of scanning a network to find the devices and their open ports running on them , it gives the basic idea of network structure and helps us to map the devices and identify potential vulnerabilites of the running services.


here i used a tool nmap, which is open source and helps us to scan the network.

nmap -sS 192.168.0.0/24 -oN nmapscan.txt

There are multiple flags in the nmap but the flag we used here is "-sS" which stands for half open scan or stealth scan. In this scan it does not complete the full three-way-handshake instead it sends a SYN packet first if it received  a SYN-ACK packet as response it stops sending the final ACK packet which does not complete the full handshake.

The other flag i used -oN is to save the output in a file.

The output i got shows there are 4 machines are up in my network 192.168.0.0/24
The IP address are 192.168.0.1-which is the router and some other machines are 192.168.0.114 (my machine), 192.168.0.118,192.168.0.137.
All the open ports and services are saved in nmapcan.txt [nmapscan.txt](https://github.com/user-attachments/files/22459482/nmapscan.txt)
<img width="1920" height="1080" alt="Screenshot From 2025-09-22 11-56-20" src="https://github.com/user-attachments/assets/ec87ae08-4ba8-42d1-be50-bc84c0035762" />

