## Objective
Identify other hosts within the subnet

## Method
nmap -sn 172.16.134.0/24
*Just scanning for hosts, not for ports


## Results
(MAC Addresses were also displayed) <br>
Host MacOS (my device): 172.16.134.1 <br>
Windows VM: 172.16.134.129 <br>
Unknown, could be some VMWare infrastructure: 172.16.134.254 <br>
Itself: 172.16.134.128 <br>

## Summary
Using nmap, the discovery confirms a target for further testing
