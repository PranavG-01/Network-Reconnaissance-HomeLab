## Objective
Identify the open TCP ports on the target

## Method
Performing a TCP SYN port scan using Nmap (default) <br> 
nmap -sS 172.16.134.129 <br> <br>
The Windows VM firewall was temporarily disabled to allow for more accurate results

## Results
Three Open TCP Ports: <br>
Port 135 (MSRPC): a port for Windows services intercommunication. This port will always show on Windows OS <br>
Port 139 (NETBIOS-SSN): an older port used for file sharing  <br>
Port 445 (MICROSOFT-DS): the modernly used port for file sharing and network aythentication <br>

## Conclusion
Initial scans, because of the firewall, returned the response that "all 1000 ports are in ignored status." By disabling the firewall, a few services were identified. Overall these ports shows us the machine's network communication capabilities 
