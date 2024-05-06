# 4.Execution_of_NetworkCommands
NAME:M.GOKUL ANAND
REG NO:212223040049
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>
CLIENT:
```
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost'8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
  ```
  SERVER:
  ```
  import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
    ```
    TRACEROUTE COMMAND:
    ```
    from scapy.all import*     
target = ["www.google.com"]     
result, unans = traceroute(target,maxttl=32) 
print(result,unans)
```
## Output
CLIENT

![image](https://github.com/mdgj2005/4.Execution_of_NetworkCommends/assets/145533936/b08f166e-69df-466a-8e30-c4bcdbcd4fc4)

SERVER

![image](https://github.com/mdgj2005/4.Execution_of_NetworkCommends/assets/145533936/62dc9d3a-2a67-4a7b-94a3-0babaa93c2a9)

TRACEROUTE COMMAND

![image](https://github.com/mdgj2005/4.Execution_of_NetworkCommends/assets/145533936/70b9bd42-b991-496b-9ed8-ad1e850ab713)






## Result
Thus Execution of Network commands Performed 
