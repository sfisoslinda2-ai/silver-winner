
# silver-winner task 1
The goal of this task was to use Nmap to identify open ports and services running on a target machine and assess their security significance.       

This command (nmap - sV -O 192.168.0.107) detects services versions and attempts to identify the operating system.  
Important of Open Ports 
- Port 135 (MSRPC) is used for communication between Windows applications and services, it can be target by attackers if vulnerabilities exist.
- Port 139 (NetBIOS-SSN) supports file and printer sharing on Windows networks. If not properly secured, it can expose information.
- Port 445 (SMB) used for file sharing and network communication. Commonly targeted by malware and ransomware attacks. It requires proper patching and access control.

The scan also showed that SMB message signing is enabled and required, which helps protect againsts man-in-the-middle attacks by verifying the intergrity of SMB communications. 

CONCLUSION
The Nmap scan successfully identified three open ports: 135, 139, and 445. These ports are commonly associated with Windows networking services and are necessary for communication and file sharing. However, they can present security risks if not properly managed. The presence of SMB message signing indicates a positive security configuration. Overall, Nmap proved effective in identifying open ports, services, and operating system information on the target host.
