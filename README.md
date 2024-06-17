# Active Directory Project
## Objective

This project's main objective is to simulate scenarios from a defender's POV, and also from an attacker's POV. The scenarios involve attacking an Active Directory server using a Kali machine, but also analyzing ingested data from the target machine with Splunk.
### Skills Learned


### Tools Used


## Steps


## STEP 1 - Creating the network diagram of the project.
<img width="699" alt="image" src="https://github.com/carageadenis1806/Active-Directory-Project/assets/75758209/7506b5cd-9ae9-46b6-bbf4-3ea249ce8708">

## STEP 2 - Installing Virtual Machines
- Windows 10 (Target machine)

- Kali Linux (Attacking machine)

- Ubuntu Server (Splunk server)

- Windows Server 2022 (AD server)

## STEP 3 - Installing & configuring required software
- Sysmon & Splunk on Windoww Target machine and AD server

- Also creating the NAT network from the diagram and assigning static IP addresses to the machines

## STEP 4 - Installing & configuring Active Directory
![image](https://github.com/carageadenis1806/Active-Directory-Project/assets/75758209/c41b61d8-ada9-424c-a89a-7643cbbaab9a)
(1)

*Ref 1: AD server promoted to domain controller.*


![image](https://github.com/carageadenis1806/Active-Directory-Project/assets/75758209/0702aa10-c380-43d1-a1e0-b266ad1ba301)
(2)

*Ref 2: Creted two new organizational units (HR & IT) and added one user to each org unit (Andreea Savu, Mihai Popescu).*


![image](https://github.com/carageadenis1806/Active-Directory-Project/assets/75758209/61697a93-2a4e-4cfc-aea6-047a444b25e5)
(3)

*Ref 3: Added the AD domain to the target machine, then logged in succesfully to one of the accounts created.*







