### Step 5: Zenmap

Your client has asked that you help identify any vulnerabilities with their file-sharing server. Using the Metasploitable machine to act as your client's server, complete the following:

#### Command for Zenmap to run a service scan against the Metasploitable machine: 
 - nmap -sV 192.168.0.10
<br></br> 
![nmap1](https://github.com/kryshael/Week-16-Homework/blob/main/Assets/nmap1.png)
<br></br> 
#### Bonus command to output results into a new text file named `zenmapscan.txt`:
 - nmap -sV -oN zenmapscan.txt 192.168.0.10
<br></br> 
![nmap2](https://github.com/kryshael/Week-16-Homework/blob/main/Assets/nmap2.png)
<br></br> 
#### Zenmap vulnerability script command: 
 - nmap --script smb-vuln* -p 139,445 192.168.0.10
<br></br> 
![nmap3](https://github.com/kryshael/Week-16-Homework/blob/main/Assets/nmap3.png)
<br></br> 
- Once you have identified this vulnerability, answer the following questions for your client:

  #### 1. What is the vulnerability:
   - SMB
  
  #### 2. Why is it dangerous:
   - If an attacker gains access, then they can easily move laterally across a data center

  #### 3. What mitigation strategies can you recommendations for the client to protect their server:
   - US-CERT recommends that users and administrators:
    - Disable SMBv1
    - Block all versions of SMB at the network boundary by blocking TCP port 445 with related protocols on UDP ports 137-138 and TCP port 139 for all boundary devices
   - #### US-CERT cautions users and administrators that disabling or blocking SMB may create problems by obstructing access to shared files, data, or devices. The benefits of mitigation should be weighed against potential disruptions to users.
    


