# THM-Offensive-Defensive-Security
*Brief Reflection and for Recollection.* 😼

**Offensive Security** - is the process of breaking into computer systems, exploiting software bugs, and finding loopholes in applications to gain unauthorized access to them.
- breaking into systems (Red team/Pentesters)
- they simulate a hacker's actions to find vulnerabilities in a system.

### 1st Hacking Simulation [http://fakebank.com]
Step 1) Open a terminal 

Step 2) Find hidden website pages
        Type the following command into the terminal to find potentially hidden pages on FakeBank's website using *GoBuster* (a command-line security application)
        
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

-Digital Forensics
-Incident Response
-Malware Analysis

**Digital Forensics** -  the focus of digital forensics shifts to analyzing evidence of an attack and its perpetrators and other areas such as intellectual property theft, cyber espionage, and possession of unauthorized content. Consequently, digital forensics will focus on different areas such as:

- File System: Analyzing a digital forensics image (low-level copy) of a system’s storage reveals much information, such as installed programs, created files, partially overwritten files, and deleted files.

- System memory: If the attacker is running their malicious program in memory without saving it to the disk, taking a forensic image (low-level copy) of the system memory is the best way to analyze its contents and learn about the attack.

- System logs: Each client and server computer maintains different log files about what is happening. Log files provide plenty of information about what happened on a system. Some traces will be left even if the attacker tries to clear their traces.

- Network logs: Logs of the network packets that have traversed a network would help answer more questions about whether an attack is occurring and what it entails.

**Incident Response** -refers to a data breach or cyber attack; however, in some cases, it can be something less critical, such as a misconfiguration, an intrusion attempt, or a policy violation.

**Malware Analysis** - Malware stands for *malicious software*. Software refers to programs, documents, and files that you can save on a disk or send over the network. Malware includes many types, such as:

Virus - is a piece of code (part of a program) that attaches itself to a program. It is designed to spread from one computer to another; moreover, it works by altering, overwriting, and deleting files once it infects a computer. The result ranges from the computer becoming slow to unusable.

Trojan Horse - is a program that shows one desirable function but hides a malicious function underneath. For example, a victim might download a video player from a shady website that gives the attacker complete control over their system.

Ransomware - is a malicious program that encrypts the user’s files. Encryption makes the files unreadable without knowing the encryption password. The attacker offers the user the encryption password if the user is willing to pay a “ransom.”

---work in progress---
