# Active Directory Project
## Objective

This project's main objective is to simulate scenarios from a defender's POV, and also from an attacker's POV. The scenarios involve attacking an Active Directory server using a Kali machine, but also analyzing ingested data from the target machine with Splunk.
### Skills Learned
- NAT network VM configuration
- AD server configuration
- Generate telemetry with Crowbar's brute force attack
- Investigate and analyze telemetry using Splunk

### Tools Used
- Splunk
- Sysmon
- Crowbar
- Virtual Box

## Steps


## STEP 1 - Creating the network diagram of the project.
<img width="943" alt="image" src="https://github.com/carageadenis1806/Active-Directory-Project/assets/75758209/90b39e91-026e-49e2-b337-96896419d675">

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

*Ref 2: Created two new organizational units (HR & IT) and added one user to each org unit (Andreea Savu, Mihai Popescu).*


![image](https://github.com/carageadenis1806/Active-Directory-Project/assets/75758209/61697a93-2a4e-4cfc-aea6-047a444b25e5)
(3)

*Ref 3: Added the AD domain to the target machine, then logged in succesfully to one of the accounts created.*


## STEP 5 - Perform a Brute Force Attack using Kali and investigate the telemetry via Splunk

![image](https://github.com/carageadenis1806/Active-Directory-Project/assets/75758209/e6733467-c9fe-4115-a439-d859c5e7e4b5)
(1)

*Ref 1: The tool crowbar provided a wordlists of passwords, then I added the AD user password to it in order to exploit it.*
![image](https://github.com/carageadenis1806/Active-Directory-Project/assets/75758209/6d7b6b2b-200a-4b1e-aa57-4cd5b4f48850)
(2)

*Ref 2: Also with the tool crowbar I managed to launch a brute force attack on AD user 'sandreea', using RDP protocol.*

## STEP 6 - Investigating the telemetry with Splunk
![image](https://github.com/carageadenis1806/Active-Directory-Project/assets/75758209/9f5c9de7-0bb6-49c5-a764-ff676d3abeec)
(1)

*Ref 1: After filtering the search to only show data from user 'sandreea', we can see under Event ID, that the event id 6425 had a count of 80. Event 6425 refers to 'An account failed to log on'. Which means that the Brute Force attack tried 80 times before getting access.*

![image](https://github.com/carageadenis1806/Active-Directory-Project/assets/75758209/4385f365-19a2-4dc0-85e1-932241200cba)
(2)


*Ref 2: After further filtering the search by adding EventID=6425, we can investigate an entry and see that the attempt was from the Kali machine.*






