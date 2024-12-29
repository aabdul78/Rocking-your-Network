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

![image](https://github.com/user-attachments/assets/87d5d9bf-0c68-4805-b258-ef1d69696715


Phase 3: "I Feel a DNS Change Comin' On"

first i remote log in to their computer using the user and passowrd i was giving

ssh jimi@167.172.144.11 yes password hendrix

then i used this commend to find out about what rockStar Corp recently reported, and why that they are unable to access rollingstone.com

cat /etc/hosts then i exit there server and u use this command:

exit after that i use my lookup command to find out the domain associated to an IP address

nslookup 98.137.246.8

Summary

this hacker has the server and modified the /etc/hosts file to point traffic to another domain. This can be confirmed using nslookup, and my findings are a malicous, in fact point to an unexpected domain. i strongly recommend to closed the port and cotinues monitering their Apllication layer.

OSI Layer - Application Layer
