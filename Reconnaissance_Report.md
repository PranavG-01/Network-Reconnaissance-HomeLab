# Home Lab Reconnaissance Report
Target IP: 172.16.134.129<br>
Device Type: Windows 10 VM<br>
Assessment: Internal Network Enumeration

## Objective
The goal of this project was to learn to practice using Nmap, identify open ports, and utilize SMB services on the target host to identify exposed services and security risks.

## Methodology
An initial scan was conducted to confirm the target IP address. Then, port scanning, OS detection, and version detection was done using Nmap. This is the script for the specific SMB enumeration:<br>
<br>
sudo nmap --script smb-os-discovery 172.16.134.129 <br>
<br>
The following TCP ports were identified from service detection:<br>
| Port | Service | Description | 
|------|---------|-------------|
| 135  |  MSRPC  | remote procedure call |
| 139  | NETBIOS-SSN | netbios session service
| 445  | MICROSOFT-DS | smb protocol |
