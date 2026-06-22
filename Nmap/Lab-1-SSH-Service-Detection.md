 Lab 1 - SSH Service Detection

1.Objective

Learn how to use Nmap to identify open ports and detect running services.

2.Environment

-Ubuntu VM (VirtualBox)
-Nmap installed
-OpenSSH Server installed


3. Commands used
   
- nmap localhost

- nmap -sV localhost
  
- ss -tuln

4. Findings

-Port 22/TCP was open.
-SSH service was detected.
-OpenSSH 7.2 was identified.
-SSH Protocol 2.0 was in use.

5. Analysis

- Nmap was able to communicate with the SSH service and identify the software version without logging into the server.

6. What I Learned

- Open ports indicate listening services.
-  Port 22 is commonly used for SSH.

7.  Verification

The command 'ss -tuln' was used to verify that the SSH service was listening on Port 22.

Output showed:

-SSH listening on IPv4 ('*:22')
-SSH listening on IPv6 (':::22')

This confirmed the Nmap scan results.

* Nmap version detection can identify software versions.
* An open port does not automatically mean a system is vulnerable.
