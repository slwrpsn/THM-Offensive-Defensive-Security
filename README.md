[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&pause=1000&color=1855CD&center=true&vCenter=true&multiline=true&width=435&lines=THM-Offensive-Defensive-Security)](https://git.io/typing-svg)

*Brief Reflection and for Recollection.* 😼

**Offensive Security** - is the process of breaking into computer systems, exploiting software bugs, and finding loopholes in applications to gain unauthorized access to them.
- breaking into systems (Red team/Pentesters)
- they simulate a hacker's actions to find vulnerabilities in a system.

### 1st Hacking Simulation [http://fakebank.com]
Step 1) Open a terminal 

Step 2) Find hidden website pages
        Type the following command into the terminal to find potentially hidden pages on FakeBank's website using *GoBuster* (a command-line security application)

![Buster Call from One Piece](https://github.com/user-attachments/assets/19d06a68-f95a-44f3-bd95-339729b089b0)


`gobuster -u http://fakebank.com -w wordlist.txt dir`

`-u` is used to state the website we're scanning
`-w`  takes a list of words to iterate through to find hidden pages

Output:
```
ubuntu@tryhackme:~/Desktop$ gobuster -u http://fakebank.com -w wordlist.txt dir
=====================================================
Gobuster v2.0.1
=====================================================
[+] Mode         : dir
[+] Url/Domain   : http://fakebank.com/
[+] Threads      : 10
[+] Wordlist     : wordlist.txt
[+] Status codes : 200,204,301,302,307,403
[+] Timeout      : 10s
=====================================================
2022/04/11 18:23:28 Starting gobuster
=====================================================
/images (Status: 301)
/DIRECTORY_NAME_OUTPUT or /bank-transfer (Status: 200)
=====================================================
2022/04/11 18:23:38 Finished
=====================================================
```

Step 3) Hack the bank
 It should be like this: 
 fakebank.com/bank-transfer

This page allows an attacker to steal money from any bank account, which is a critical risk for the bank. As an ethical hacker, you would (with permission) find vulnerabilities in their application and report them to the bank to fix before a hacker exploits them.

(The rest of simulation are located at Intro to Offensive Security- Task 2)

**Defensive Security** - is somewhat the opposite of offensive security, as it is concerned with two main tasks:

1. Preventing intrusions from occurring
2. Detecting intrusions when they occur and responding properly

- Prevention/Detecting Intrusions (Blue team/SOC)
- User cyber security awareness
- Documenting and managing assets
- Updating and patching systems
- Setting up preventative security devices: Firewall and Intrusion Prevention systems (IPS)
- Setting up logging and monitoring devices

**Areas of Defensive Security**

> Security Operations Center (SOC) - Threat Intelligence
> Digital Forensics and Incident Response (DFIR) - Malware Analysis

**Security Operations Center** - a team of cyber security professionals that monitors the network and its systems to detect malicious cyber security events.
They cover:
Vulnerabilities, Policy violations, Unauthorized activity, Network intrusions

Security operations cover various tasks to ensure protection; one such task is threat intelligence.

**Threat Intelligence** - Intelligence needs data so once we detect the threat, we can predict their activity, action and we’ll be able to mitigate their attacks and prepare an effective response strategy.

**Digital Forensics and Incident Response (DFIR)** 

It covers:

+ Digital Forensics
+ Incident Response
+ Malware Analysis

**Digital Forensics** -  the focus of digital forensics shifts to analyzing evidence of an attack and its perpetrators and other areas such as intellectual property theft, cyber espionage, and possession of unauthorized content. Consequently, digital forensics will focus on different areas such as:

- File System: Analyzing a digital forensics image (low-level copy) of a system’s storage reveals much information, such as installed programs, created files, partially overwritten files, and deleted files.

- System memory: If the attacker is running their malicious program in memory without saving it to the disk, taking a forensic image (low-level copy) of the system memory is the best way to analyze its contents and learn about the attack.

- System logs: Each client and server computer maintains different log files about what is happening. Log files provide plenty of information about what happened on a system. Some traces will be left even if the attacker tries to clear their traces.

- Network logs: Logs of the network packets that have traversed a network would help answer more questions about whether an attack is occurring and what it entails.

**Incident Response** -refers to a *data breach or cyber attack* ; however, in some cases, it can be something less critical, such as a misconfiguration, an intrusion attempt, or a policy violation.

The four major phases of the incident response process are:

**Preparation**: This requires a team trained and ready to handle incidents. Ideally, various measures are put in place to prevent incidents from happening in the first place.

**Detection and Analysis**: The team has the necessary resources to detect any incident; moreover, it is essential to further analyze any detected incident to learn about its severity.

**Containment, Eradication, and Recovery**: Once an incident is detected, it is crucial to stop it from affecting other systems, eliminate it, and recover the affected systems. For instance, when we notice that a system is infected with a computer virus, we would like to stop (contain) the virus from spreading to other systems, clean (eradicate) the virus, and ensure proper system recovery.

**Post-Incident Activity**: After successful recovery, a report is produced, and the learned lesson is shared to prevent similar future incidents

![image](https://github.com/user-attachments/assets/7df13329-eca4-4c79-aafb-bbe4aef063ab)

> [!CAUTION]
> Negative potential consequences of an action. (Kidding. Just always be careful w/ anything you use and click inside the cyberworld.)

**Malware Analysis** - Malware stands for *malicious software*. Software refers to programs, documents, and files that you can save on a disk or send over the network. Malware includes many types, such as:

**Virus** - is a piece of code (part of a program) that attaches itself to a program. It is designed to spread from one computer to another; moreover, it works by altering, overwriting, and deleting files once it infects a computer. The result ranges from the computer becoming slow to unusable.

**Trojan Horse** - is a program that shows one desirable function but hides a malicious function underneath. For example, a victim might download a video player from a shady website that gives the attacker complete control over their system.

**Ransomware** - is a malicious program that encrypts the user’s files. Encryption makes the files unreadable without knowing the encryption password. The attacker offers the user the encryption password if the user is willing to pay a “ransom.”

<ins>Malware analysis</ins> have two ways to learn about such malicious programs using various means like:

1.) Static Analysis- works by inspecting the malicious program without running it. Usually, this requires solid knowledge of assembly language (processor’s instruction set, i.e., computer’s fundamental instructions).

2.) Dynamic Analysis- works by running the malware in a controlled environment and monitoring its activities. It lets you observe how the malware behaves when running.

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=15&pause=1000&color=18CD3B&center=true&vCenter=true&multiline=true&width=435&lines=Practical+Example+of+Defensive+Security)](https://git.io/typing-svg)

![image](https://github.com/user-attachments/assets/897bf1ef-d18e-4f7a-b531-1fe5c08d696d)

In a Security Operations Center (SOC) for a bank, a Security Information and Event Management (SIEM) system is used to monitor security events. It alerts us to issues like failed login attempts or logins from unusual locations, as well as unusual behaviors detected by machine learning.

When an event is flagged in red, we investigate it further to determine its cause, which could involve a local user, a computer, or a remote IP address. If we confirm the event is malicious, we take action by reporting it and potentially blocking the suspicious IP address.

Instructions:
Inspect the alerts in your SIEM dashboard. Find the malicious IP address from the alerts, make a note of it, and then click on the alert to proceed.

Alert Log:

Date                       /                          Message

$\color{green}{November\ 10th\ 2024,\ 03:19:21:124\ Successful\ SSH\ authentication\ attempt\ to\ port\ 22\ from\ IP\ address\ 143.110.250.149}$

$\color{red}{November\ 10th\ 2024\ 03:16:23:111\ Unauthorized\ connection\ attempt\ detected\ from\ IP address\ 143.110.250.149\ to\ port\ 22}$

$\color{green}{November\ 10th\ 2024,\ 00:59:33:276\ The\ user\ John\ Doe\ logged\ in\ successfully\ (Event\ ID\ 4624)}$

$\color{green}{November\ 10th\ 2024,\ 00:59:53:204\ Multiple\ failed\ login\ attempts\ from\ John\ Doe}$

$\color{green}{November\ 10th\ 2024,\ 00:49:04:284\ Logon\ Failure:\ Specified\ Account's\ Password\ Has\ Expired\ (Event\ ID\ 535)}$

There are websites on the Internet that allow you to check the reputation of an IP address to see whether it's malicious or suspicious.

143.110.250.149 was the IP ADDRESS of the suspicious ant, so therefore we will use the IP Scanner to check it.

There are many open-source databases out there, like **AbuseIPDB**, and **Cisco Talos Intelligence**, where you can perform a reputation and location check for the IP address. Most security analysts use these tools to aid them with alert investigations. You can also make the Internet safer by reporting the malicious IPs, for example, on AbuseIPDB.

Now that we know the IP address is malicious, we need to escalate it to a staff member!

The results:

143.110.250.149 was found in our database!

Confidence of the IP being malicious is 100%

Malicious

ISP:	China Mobile Communications Corporation

Domain Name:	chinamobileltd.thm

Country:	China

City:	Zhenjiang, Jiangsu

> [!NOTE]
> Any suspicious or malicious attempts should be escalated to the appropriate department, specifically to the Team Leader of the SOC (Security Operations Center) team.

You got the permission to block the malicious IP address, and now you can proceed and implement the block rule. Block the malicious IP address on the firewall and find out what message they left for you

Previous IP ADDRESS of the suspicious ANT: 143.110.250.149 

After that, We should Block it to prevent another case to occur again.

**You blocked the malicious IP address!**

$\color{red}{\text{THM-\{THREAT-BLOCKED\}}}$

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=15&pause=1000&color=FF0000&center=true&vCenter=true&multiline=true&width=444&lines=Congratulations!+You+Captured+Another+FLAG+%F0%9F%9A%A9)](https://git.io/typing-svg)


