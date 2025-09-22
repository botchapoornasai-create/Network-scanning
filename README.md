# Network-scanning

DEF-network scanning is the process of scanning a network to find the devices and their open ports running on them , it gives the basic idea of network structure and helps us to map the devices and identify potential vulnerabilites of the running services.


here i used a tool nmap, which is open source and helps us to scan the network.

nmap -sS 192.168.0.0/24 -oN nmapscan.txt

There are multiple flags in the nmap but the flag we used here is "-sS" which stands for half open scan or stealth scan. In this scan it does not complete the full three-way-handshake instead it sends a SYN packet first if it received  a SYN-ACK packet as response it stops sending the final ACK packet which does not complete the full handshake.

The other flag i used -oN is to save the output in a file.
