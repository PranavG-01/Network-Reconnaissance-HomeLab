# Objective 
Detect the operating system of the target host

## Method
Performed the nmap OS detection scan <br>
nmap -O 172.16.134.129 <br>
<br>
A more aggressive approach was also used <br>
sudo nmap -O --osscann-guess 172.16.134.129

## Results
From the initial approach the returned response was "No exact OS matches for host."<br>
After attempting the more aggressive command, this was the response:<br>
Aggressive OS guesses: Microsoft Windows 10 1703 or Windows 11 21H2 (99%), Microsoft Windows 11 21H2 (98%), Microsoft Windows 10 1507 - 1607 (97%), Microsoft Windows 10 1511 (97%), Microsoft Windows Server 2022 (97%), Microsoft Windows 10 1703 (96%), Microsoft Windows Longhorn (95%), Microsoft Windows 10 1511 - 1607 (94%), Microsoft Windows Server 2008 (94%), Microsoft Windows Vista SP2 or Windows 7 or Windows Server 2008 R2 or Windows 8.1 (94%)

## Conclusion
From the initial approach, OS fingerprintng didn't produce an exact match. Modern Windows systems combined with firewall protection and being inside a VM is theorized to have limited the responses. Though, the produced outputs from Port_Scanning strongly indicate that the target host is running a Windows OS. Then, this is also seen from the more aggressive approach that the OS is likely Windows. 
