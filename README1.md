#Ubuntu Network and SSH project

the purpose of this project is to creat two virtual machines that can communicate with each other ovwe a network and share data.

##Tools and Technologies
-Ubuntu
-Virtualbox
-SSH
-ping
-scp

##Network Setup
Two Ubuntu virtual machines were connected using VirtualBox NAT Network

-Server IP: 10.0.2.10
-Client IP: 10.0.2.20
-Network: NatNetwork

##Network Setup
First, I tried to use DHCP, but both virtual machines got the same IP addresses
Then, I created a NAT Network in VirtualBox and assigned static IP addresses to both  machines.
Finally, I tested the connection between the tow virtual machines using ping.The connection was successful. 




##SSH Configuration 
I installed and enabled the SSH service on the server.
Then, I connected to the server from the client using SSH and a password.
the connection was successful.


##SSH Key Authentication 
I created an SSH key onthe client and copied it to the server.
Then, I connected to the server using the SSH key without entering a password.

##File Transfer 
I transferred a test file from the client to the server using SCP.
Then, I compared the SHA256 hashes of both files.The hashes matched, confirming that the files were identical.


##Troubleshooting
I tested file permissions on the server.
I checked whether another user cloud read the file. Access was allowed when the permissions were correct and denied when the permissions were restricted.

###Eror1:Wrong SSH port

I tried to connect to the server using port 2222.
The connection failed with "Connection refussed".
This showed that SSH that was not listening on that pport.

###Erroe 2:wrong Username

I tride to connect to the server using an incorrect username.
The connection failed with "Permission denied".
This showed that the username was incorrect.

###Error 3: SSH Service Stopped
I stopped the service on the server.
when I tried to connect from the client, the connection failed with "Connection refused".
I started the SSH service again and checked that it was running.

##Conclusion
In this project, I learned how to connect two Ubuntu machines, configure SSH, transfer files, and manage file permissions.











