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
Common services running in my result are SSH,HTTP,DNS.

#wireshark

DEF- wireshark is a free open source network protocol analyzers which captures the traffic flowing from your network interface card.
Here we are seeing the traffic generated from our nmap scan.

Once you opend the wireshark you can see the interface with all the adapter of your machine and the one with network traffic.
<img width="1919" height="1044" alt="Screenshot From 2025-09-26 14-50-43" src="https://github.com/user-attachments/assets/e9734eb7-ec2c-4ca3-b587-fe4bce2aabce" />

All the traffic generated from our scan is visible in image.
<img width="1920" height="1080" alt="Screenshot From 2025-09-22 18-21-08" src="https://github.com/user-attachments/assets/b6dfbad0-d245-446b-ad77-e536342f1aa3" />

We can also see a particular packets individual layers data information from the bottom left tab in the wireshark.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7d382327-58b9-4902-afc9-c705a7d8ba4f" />
