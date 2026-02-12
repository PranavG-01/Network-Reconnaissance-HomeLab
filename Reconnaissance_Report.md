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
| 445  | MICROSOFT-DS | smb protocol | <br>

Individual descriptions of these ports are in the Port_Scanning+SMB_Enumeration file <br>

## SMB Enumeration
The aforementioned script did not return additional details such as hostname, domain name, OS information, or file information

## Assessment
The SMB related ports can be leveraged for attacks within an internal network. While in this lab no information was given, SMB protocol services still remain as targets for exploitation or credential harvesting (in the case that it's not well protected). In this lab it's evident that, at the least, basic security regulations are in place.

## Conclusion
Within the target Windows VM, no anonymous access vulnerabilities were identified. Though, further testing (vulnerability scanning for SMB exploits, authenticated SMB enumeration, share-specfiic access testing, etc.) can be completed for a deeper understanding of the system's security and other potential misconfigurations. Overall, SMB services still remain a common gateway for internal network attacks thus should be monitored regularly. 
