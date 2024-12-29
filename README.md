# Rocking-your-Network
Homework 8

step one "I'd like to Teach the World to Ping"

List the steps and commands used to complete the tasks.

fping 167.172.144.11

List any vulnerabilities discovered.

i discovered that IP adress 167.172.144.11 is a life

List any findings associated to a hacker. four ip adresses are shows unreachable but there is only one ip adress that shows alive ip adress

167.172.144.11 is alive
15.199.94.91 is unreachable
11.199.158.91 is unreachable
11.199.141.91 is unreachable
15.199.95.91 is unreachable

Summary

I ran nping against the four ip addresses hosted in Hollywood, only one of which (167.172.144.11) shows alive. this is the network layer. This could be the result of a hacker having a access to one of Rockstar Corp's servers and having opened a port. i recomended to closed that port before the hacker gaines more information from the rockstar corp's.

This occurred on the network layer

![image](https://github.com/user-attachments/assets/c3b39f34-cdb5-4106-b6ce-22538222c305)

Phase 2: "Some Syn for Nothin`"

Run a SYN SCAN against the IP accepting connections. See SYN SCAN Instructions below.

sudo nmap -sS 167.172.144.11

Using the results of the SYN SCAN, determine which ports are accepting connections.

port 22/tcp is open

Summary

we can see that an ssh port is open, also number of remote access service ports. the hacker is using the trasport layer for web crawling TCP, UDP. this hacker is doing alot more damage if its continues to have accsess on this open port. i recomended to rockstar corp' to close this port or aither have very strong firewall.

port 22\tcp is part of the transport layer

![image](https://github.com/user-attachments/assets/91454a7b-9d1f-4f94-8c53-bcc58727ce04)



Phase 3: "I Feel a DNS Change Comin' On"

first I remote log in to their computer using the user and passowrd I was given

ssh jimi@167.172.144.11 yes password hendrix

then I used this commend to find out about what rockStar Corp recently reported, and why that they are unable to access rollingstone.com

cat /etc/hosts then i exit there server and u use this command:

exit after that I use my lookup command to find out the domain associated to an IP address

nslookup 98.137.246.8

Summary

This hacker has the server and modified the /etc/hosts file to point traffic to another domain. This can be confirmed using nslookup, and my findings are a malicous, in fact point to an unexpected domain. I strongly recommend to closed the port and cotinue monitering their apllication layer.

OSI Layer - Application Layer

![image](https://github.com/user-attachments/assets/deeafb9e-96fd-4cdb-8d98-6733b17ad035)

![image](https://github.com/user-attachments/assets/52cea197-c438-43d8-a0e7-f2646cd4dacc)

Phase 4: "ShARP Dressed Man"

Within the RockStar server that you SSH'd into, and in the same directory as the configuration file from Phase 3, the hacker left a note as to where he stored away some packet captures.

ssh jimi:167.172.144.11 password hendrix then i use this command to list all the directories and files inside etc

ls /etc/ then in order to View the file to find where to recover the packet captures. then i use this command

cat /etc/packetcaptureinfo.txt packetcapture : Captured Packets are here: https://drive.google.com/file/d/1ic-CFFGrbruloYrWaw3PvT71elTkh3eF/view?usp=sharing

![image](https://github.com/user-attachments/assets/ef0ad812-03f6-4fd8-8d47-a4cbeaaea172)

![image](https://github.com/user-attachments/assets/aea29395-c70c-40d0-be59-a381854c0642)

![image](https://github.com/user-attachments/assets/72d5d600-f711-4951-853d-7ef7a2081177)


Summary

I find out the hacker had a massege or note he or she left behind, offering up sensitive information - an open ssh port with user creds in exchange for one million dollars, my result of the hacker redirecting network traffic or backdooring into RockStar Corp's server, set in the server's /etc/hosts. Rockstar corp' should have their firewall denied any unauthorized traffic on port 22 and check for any network modifications. Hacker has MAC address of Frame 1: 42 bytes on wire (336 bits), 42 bytes captured (336 bits) on interface unknown, id 1 this hacker is using OSI layer network layer.






