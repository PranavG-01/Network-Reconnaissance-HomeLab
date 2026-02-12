Environment:
  Kali Linux (latest ISO file)
  Windows 10 (Downloaded directly from VMWare Fusion)

IP Addresses:
  Kali Linux (ip a):
    IP Address: 172.16.134.128
    Subnet Mask: 255.255.255.0
    Default Gateway: 172.16.134.2
    
  Windows 10 (ipconfig): 
    IP Address: 172.16.134.129
    Subnet Mask: 255.255.255.0
    Default Gateway: 172.16.134.2

NAT Configuration + DHCP IP Assignment:
  In a NAT (Network Address Translation) setup, the virtual machines are given private addresses, which can communicate with the internet by translating into the device's public IP address. Though, the VM doesn't actually appear on the network. This is all possible through the Dynamic Host Configuration Protocol (DHCP), which automatically configures all the VMs' IP addresses and network settings. Additionally, a virtual switch enables communication between the two machines (layer 2 connectivity). 

Limitations:
  Lab operates within 1 subnet
  Internet access may be restricted depending on routing availability
