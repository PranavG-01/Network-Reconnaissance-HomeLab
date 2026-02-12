# Objective 
Detect the operating system of the target host

## Method
Performed the nmap OS detection scan <br>
nmap -O 172.16.134.129 <br>
<br>
A more aggressive approach was also conducted using OS guessing <br>
sudo nmap -O --osscann-guess 172.16.134.129

## Results
The initial approach returned:<br> 
"No exact OS matches for host."<br>
After attempting OS guessing, Nmap produced a list of potential matches:<br>
Microsoft Windows 10 1703 or Windows 11 21H2 (99%), Microsoft Windows 11 21H2 (98%), Microsoft Windows 10 1507 - 1607 (97%), Microsoft Windows 10 1511 (97%), Microsoft Windows Server 2022 (97%), Microsoft Windows 10 1703 (96%), Microsoft Windows Longhorn (95%), Microsoft Windows 10 1511 - 1607 (94%), Microsoft Windows Server 2008 (94%), Microsoft Windows Vista SP2 or Windows 7 or Windows Server 2008 R2 or Windows 8.1 (94%)

## Conclusion
The initial setback suggests that firewall protection and being inside a VM is may have limited the accuracy of OS fingerprinting. Modern Windows systems also tend to restrict network recconnaissance. However, the produced outputs from Port_Scanning strongly indicate that the target host is running a Windows OS. This is also seen from the more aggressive approach, that the OS is likely Windows, with high confidence.
