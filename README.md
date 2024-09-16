# Linux
### Bash Shell

```
(timeout 2 bash -c '</dev/tcp/127.0.0.1/5000 && echo PORT OPEN || echo PORT CLOSED') 2>/dev/null
```
![image](https://user-images.githubusercontent.com/12382861/146758294-3adb5135-cdde-47b8-a99b-b3127440e0e6.png)

### Netcat
check
```
nc -zv 127.0.0.1 5000
```
-z = sets nc to simply scan for listening daemons, without actually sending any data to them  
-v = enables verbose mode

stream
```
nc 127.0.0.1 5000
```

### nmap 
```bash
nmap -sS -p- 0.0.0.0
```
-p- will scan all ports other than common once ( recomended )
-sS stelth scan to void logging

non-root user
```bash
nmap -sT 0.0.0.0
```
root user 
```bash
nmap -sS 0.0.0.0
```

![image](https://user-images.githubusercontent.com/12382861/146760517-6450f53e-9ef4-4b37-b334-ff35ee17c524.png)


added new branch




# Windows CMD
## curl

```
curl -vv telnet://localhost:5000
```
success
```
*   Trying 127.0.0.1:5000...
* TCP_NODELAY set
* Connected to localhost (127.0.0.1) port 5000 (#0)
```
failure
```
*   Trying 127.0.0.1:960...
* TCP_NODELAY set
* connect to 127.0.0.1 port 960 failed: Connection refused
* Failed to connect to localhost port 960: Connection refused
* Closing connection 0
curl: (7) Failed to connect to localhost port 960: Connection refused
```


https://stackoverflow.com/questions/48198/how-can-you-find-out-which-process-is-listening-on-a-tcp-or-udp-port-on-windows
https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax

# Windows Powershell
### Test-NetConnection
```
Test-NetConnection -ComputerName vishalmamidi.com -Port 443
```

### netstat
```
netstat -a -n -o 
```
```
netstat -a -n -o | findstr :5044
```
![image](https://user-images.githubusercontent.com/12382861/146552070-6ac75724-6ee8-4b92-9c5b-1e056f46cf86.png)

### Get-NetTCPConnection
```
Get-NetTCPConnection -LocalPort 9600 | Format-List
```
![image](https://user-images.githubusercontent.com/12382861/146554252-c48d4945-ca39-4fe4-a18e-b518df416d98.png)

### TCPView Sysinternals 

https://docs.microsoft.com/en-in/sysinternals/downloads/tcpview


[TCPView.zip]
(https://github.com/vishalmamidi/port_ping_check_tcp/files/7735598/TCPView.zip)



### Telnet
```
telnet <ip-address or host> <port>
telnet google.com 443
```
![image](https://user-images.githubusercontent.com/12382861/146546534-3d296fb9-4742-4331-89af-8b45ea0c1b4a.png)
![image](https://user-images.githubusercontent.com/12382861/146751763-171e732b-dae9-4dcf-a3e1-212e7fc1c293.png)


