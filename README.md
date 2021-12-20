# Windows Powershell
https://stackoverflow.com/questions/48198/how-can-you-find-out-which-process-is-listening-on-a-tcp-or-udp-port-on-windows

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



