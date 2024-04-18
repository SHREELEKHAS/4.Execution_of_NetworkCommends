## SHREE LEKHA.S (212223110052)
# 4.Execution_of_NetworkCommands
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

## Program:
```
server.py
import socket

s = socket.socket()
s.connect(('localhost', 8000))

while True:
    ip = input("Enter the website you want to ping: ")
    s.send(ip.encode())
    print(s.recv(1024).decode())

```

```
client.py
import socket
from pythonping import ping

s = socket.socket()
s.bind(('localhost', 8000))
s.listen(5)
c, addr = s.accept()

while True:
    hostname = c.recv(1024).decode()
    try:
        c.send(str(ping(hostname, verbose=False)).encode())
    except KeyError:
        c.send("Not Found".encode())

```

## PING command:
## PING Program:
![Screenshot 2024-04-19 001123](https://github.com/SHREELEKHAS/4.Execution_of_NetworkCommends/assets/149768910/73761097-07f8-48ac-b9a7-1c63a11cb748)

## PING command output:
![Screenshot 2024-04-19 001057](https://github.com/SHREELEKHAS/4.Execution_of_NetworkCommends/assets/149768910/91b54ca8-5add-44a8-b03f-79b425134a3e)


## TRACERT command:
## TRACERT program:

![Screenshot 2024-04-18 231236](https://github.com/SHREELEKHAS/4.Execution_of_NetworkCommends/assets/149768910/a84d757e-cd0c-4f77-9403-e608368087b0)

## TRACERT command output:
![Screenshot 2024-04-18 231236](https://github.com/SHREELEKHAS/4.Execution_of_NetworkCommends/assets/149768910/7dd24002-595c-4d33-a7b5-e7fa44965100)

## Result
Thus Execution of Network commands Performed 
