## Objective
Identify other hosts within the subnet

## Method
nmap -sn 172.16.134.0/24
*Just scanning for hosts, not for ports


## Results
(MAC Addresses were also displayed)
Host MacOS (my device): 172.16.134.1
Windows VM: 172.16.134.129
Unknown, could be some VMWare infrastructure: 172.16.134.254
Itself: 172.16.134.128

## Summary
Using nmap, the discovery confirms a target for further testing
