---
title: INVESTIGATING-WINDOW(THM)

---

# Basic server-side template injection(ERB template)

### ***WHAT IS OUR TASK?***
This is a challenge that is exactly what is says on the tin, there are a few challenges around investigating a windows machine that has been previously compromised.

Connect to the machine using RDP(Remote Desktop Protocol is a protocol used to establish remote graphical sessions over the network.). The credentials the machine are as follows:

Username: Administrator
Password: letmein123!
## ***SOLUTION***
1. Whats the version and year of the windows machine?

in this question i go to system infomation and i found that this is *Windows Server 2016* ![w1 (Edited)](https://hackmd.io/_uploads/SksA_sq-Mx.png)



2. Which user logged in last?

the last logged in is Administrator by inpecting all users acconts their times to login in the system
#### COMMAND THAT I USE

net user --> to list all users in the system

net user Administator --> i find the last user to login in the system
![w2](https://hackmd.io/_uploads/H18Nosq-Mx.png)


3. When did John log onto the system last?
#### COMMAND THAT I USE
net user John --> shows the time that login in the system
![w3](https://hackmd.io/_uploads/H1PyhocWGe.png)

4. What IP does the system connect to when it first starts?

this is shown first when the system is up 10.34.2.3
![w4](https://hackmd.io/_uploads/rkpPnicbMg.png)

5. What two accounts had administrative privileges (other than the Administrator user)?

Answer format: List them in alphabetical order.

#### COMMAND THAT I USE
net localgroup Administrators –> to list all Administrators in the system

and the aswer according to the order are "Guest, Jenny"
![w5](https://hackmd.io/_uploads/ByVYCs5bzx.png)


6. Whats the name of the scheduled task that is malicous.

This question i found in the Task schedular and it is listed as *Clean file system* because it runs everyday 
![w6](https://hackmd.io/_uploads/ry5s13cZMg.png)

7. What file was the task trying to run daily?

the file that runs daily is *nc.ps1* as shown in the above picture qustion no.6

8. What port did this file listen locally for?

the port that is used to this file listen locally is 1348 as shown in the question no. 6


9. When did Jenny last logon?

#### COMMAND THAT I USE
net user Jenny --> shows the time that login in the system. this is like we found in the question no. 3 & the answer is *Never*
![w9](https://hackmd.io/_uploads/BJnJM2qWzg.png)


10. At what date did the compromise take place?

Answer format: MM/DD/YYYY

The answer of this question is 03/02/2019 because of the analysis of when the system is compromised ![w10](https://hackmd.io/_uploads/B1r97n9-ze.png)

11. During the compromise, at what time did Windows first assign special privileges to a new logon?

Answer format: MM/DD/YYYY HH:MM:SS AM/PM

the answer of this question is *03/02/2019 4:04:49 PM* that was the time of windows first assign special privileges

12. What tool was used to get Windows passwords?

The answer of this question is *Mimikatz* because of the analysis of identify the file that is trying to run malicious in the system. in the file of C:/TMP that is malicious i took the file mim.txt and tool used is Mimikatz ![w12](https://hackmd.io/_uploads/ryrjHn9Wzx.png)

13. What was the attackers external control and command servers IP?

I open the notepad to this location C:\Windows\System32\drivers\etc\hosts and i found the suspicious entries is 76.32.97.132
![w13](https://hackmd.io/_uploads/rJs08hcWGg.png)

14. What was the extension name of the shell uploaded via the servers website?

The answer of this question is *.jsp* because of the analysis of the shell uploaded via the server as shown bellow
![w14](https://hackmd.io/_uploads/BkvADnqWMe.png)

15. What was the last port the attacker opened?

the port that is open to the attacker is 1337 and this can be found in the Firewall setting as shown bellow 
![w8](https://hackmd.io/_uploads/Hy1JZh9-Ge.png)

16. Check for DNS poisoning, what site was targeted?

the answer is google.com as shown in the question no. 13
## ***CONCLUSION***
Solved by : R4soul
Udom Cybersecurity Club Member {UCC}
@2026
# Basic server-side template injection(ERB template)

### ***WHAT IS OUR TASK?***
This is a challenge that is exactly what is says on the tin, there are a few challenges around investigating a windows machine that has been previously compromised.

Connect to the machine using RDP(Remote Desktop Protocol is a protocol used to establish remote graphical sessions over the network.). The credentials the machine are as follows:

Username: Administrator
Password: letmein123!
## ***SOLUTION***
1. Whats the version and year of the windows machine?

in this question i go to system infomation and i found that this is *Windows Server 2016* ![w1 (Edited)](https://hackmd.io/_uploads/SksA_sq-Mx.png)



2. Which user logged in last?

the last logged in is Administrator by inpecting all users acconts their times to login in the system
#### COMMAND THAT I USE

net user --> to list all users in the system

net user Administator --> i find the last user to login in the system
![w2](https://hackmd.io/_uploads/H18Nosq-Mx.png)


3. When did John log onto the system last?
#### COMMAND THAT I USE
net user John --> shows the time that login in the system
![w3](https://hackmd.io/_uploads/H1PyhocWGe.png)

4. What IP does the system connect to when it first starts?

this is shown first when the system is up 10.34.2.3
![w4](https://hackmd.io/_uploads/rkpPnicbMg.png)

5. What two accounts had administrative privileges (other than the Administrator user)?

Answer format: List them in alphabetical order.

#### COMMAND THAT I USE
net localgroup Administrators –> to list all Administrators in the system

and the aswer according to the order are "Guest, Jenny"
![w5](https://hackmd.io/_uploads/ByVYCs5bzx.png)


6. Whats the name of the scheduled task that is malicous.

This question i found in the Task schedular and it is listed as *Clean file system* because it runs everyday 
![w6](https://hackmd.io/_uploads/ry5s13cZMg.png)

7. What file was the task trying to run daily?

the file that runs daily is *nc.ps1* as shown in the above picture qustion no.6

8. What port did this file listen locally for?

the port that is used to this file listen locally is 1348 as shown in the question no. 6


9. When did Jenny last logon?

#### COMMAND THAT I USE
net user Jenny --> shows the time that login in the system. this is like we found in the question no. 3 & the answer is *Never*
![w9](https://hackmd.io/_uploads/BJnJM2qWzg.png)


10. At what date did the compromise take place?

Answer format: MM/DD/YYYY

The answer of this question is 03/02/2019 because of the analysis of when the system is compromised ![w10](https://hackmd.io/_uploads/B1r97n9-ze.png)

11. During the compromise, at what time did Windows first assign special privileges to a new logon?

Answer format: MM/DD/YYYY HH:MM:SS AM/PM

the answer of this question is *03/02/2019 4:04:49 PM* that was the time of windows first assign special privileges

12. What tool was used to get Windows passwords?

The answer of this question is *Mimikatz* because of the analysis of identify the file that is trying to run malicious in the system. in the file of C:/TMP that is malicious i took the file mim.txt and tool used is Mimikatz ![w12](https://hackmd.io/_uploads/ryrjHn9Wzx.png)

13. What was the attackers external control and command servers IP?

I open the notepad to this location C:\Windows\System32\drivers\etc\hosts and i found the suspicious entries is 76.32.97.132
![w13](https://hackmd.io/_uploads/rJs08hcWGg.png)

14. What was the extension name of the shell uploaded via the servers website?

The answer of this question is *.jsp* because of the analysis of the shell uploaded via the server as shown bellow
![w14](https://hackmd.io/_uploads/BkvADnqWMe.png)

15. What was the last port the attacker opened?

the port that is open to the attacker is 1337 and this can be found in the Firewall setting as shown bellow 
![w8](https://hackmd.io/_uploads/Hy1JZh9-Ge.png)

16. Check for DNS poisoning, what site was targeted?

the answer is google.com as shown in the question no. 13
## ***CONCLUSION***
Solved by : R4soul
Udom Cybersecurity Club Member {UCC}
@2026
