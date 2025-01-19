# Introduction to Cyber Security

Understand what is offensive and defensive security, and learn about careers available in cyber.

Table of Contents

-   [Offensive Security Intro](#offensive-security-intro)
    -   [Careers](#what-careers-are-there)
-   [Defensive Security Intro](#defensive-security-intro)
    -   [Security Operation Center](#security-operations-center-soc)
    -   [Threat Intelligence](#threat-intelligence)
    -   [Digital Forensics and Incident Response](#digital-forensics-and-incident-response-dfir)
    -   [Malware Analysis](#malware-analysis)

## Offensive Security Intro

"To outsmart a hacker, you need to think like one."

This is the core of "Offensive Security."

> It involves breaking into computer systems, exploiting software bugs, and finding loopholes in applications to gain unauthorized access. The goal is to understand hacker tactics and enhance our system defences.

### What careers are there?

Here is a short description of a few offensive security roles, sometimes referred to as <font color="pink">Red Teams</font>:

-   Penetration Tester - Responsible for testing technology products for finding exploitable security vulnerabilities.
-   Red Teamer - Plays the role of an adversary, attacking an organization and providing feedback from an enemy's perspective.
-   Security Engineer - Design, monitor, and maintain security controls, networks, and systems to help prevent cyberattacks.

## Defensive Security Intro

Defensive security is concerned with two main tasks:

    1. Preventing intrusions from occurring
    2. Detecting intrusions when they occur and responding properly

<font color="lightblue">Blue teams</font> are part of the defensive security landscape.

Some of the tasks that are related to defensive security include:

-   User cyber security awareness: Training users about cyber security helps protect against attacks targeting their systems.
-   Documenting and managing assets: We need to know the systems and devices we must manage and protect adequately.
-   Updating and patching systems: Ensuring that computers, servers, and network devices are correctly updated and patched against any known vulnerability (weakness).
-   Setting up preventative security devices: firewall and intrusion prevention systems (IPS) are critical components of preventative security. Firewalls control what network traffic can go inside and what can leave the system or network. IPS blocks any network traffic that matches present rules and attack signatures.
-   Setting up logging and monitoring devices: Proper network logging and monitoring are essential for detecting malicious activities and intrusions. If a new unauthorized device appears on our network, we should be able to detect it.

There is much more to defensive security. Aside from the above, we will also cover the following related topics:

-   Security Operations Center (SOC)
-   Threat Intelligence
-   Digital Forensics and Incident Response (DFIR)
-   Malware Analysis

### Security Operations Center (SOC)

> A **Security Operations Center (SOC)** is a team of cyber security professionals that monitors the network and its systems to detect malicious cyber security events.

<small>Wiki: [SOC](https://en.wikipedia.org/wiki/Security_operations_center)</small>

Some of the main areas of interest for a SOC are:

-   **Vulnerabilities**: Whenever a system vulnerability (weakness) is discovered, it is essential to fix it by installing a proper update or patch. When a fix is unavailable, the necessary measures should be taken to prevent an attacker from exploiting it. Although remediating vulnerabilities is vital to a SOC, it is not necessarily assigned to them.
-   **Policy violations**: A security policy is a set of rules required to protect the network and systems. For example, it might be a policy violation if users upload confidential company data to an online storage service.
-   **Unauthorized activity**: Consider the case where a user’s login name and password are stolen, and the attacker uses them to log into the network. A SOC must detect and block such an event as soon as possible before further damage is done.
-   **Network intrusions**: No matter how good your security is, there is always a chance for an intrusion. An intrusion can occur when a user clicks on a malicious link or when an attacker exploits a public server. Either way, when an intrusion occurs, we must detect it as soon as possible to prevent further damage.

Security operations cover various tasks to ensure protection; one such task is _threat intelligence_.

### Threat Intelligence

> In this context, <ins>intelligence refers to information you gather about actual and potential enemies</ins>. A threat is any action that can disrupt or adversely affect a system.

Threat intelligence collects information to help the company better prepare against potential adversaries. The purpose would be to achieve a threat-informed defence.

Learning about your adversaries lets you know their tactics, techniques, and procedures. As a result of threat intelligence, we identify the threat actor (adversary) and predict their activity. Consequently, we can mitigate their attacks and prepare a response strategy.

### Digital Forensics and Incident Response (DFIR)

This section is about Digital Forensics and Incident Response (DFIR), and we will cover:

-   Digital Forensics
-   Incident Response
-   Malware Analysis

#### Digital Forensics

> Forensics is the application of science to investigate crimes and establish facts. With the use and spread of digital systems, such as computers and smartphones, a new branch of forensics was born to investigate related crimes: **computer forensics**, which later evolved into **digital forensics**.

In defensive security, the focus of digital forensics shifts to analyzing evidence of an attack and its perpetrators and other areas such as intellectual property theft, cyber espionage, and possession of unauthorized content. Consequently, digital forensics will focus on different areas, such as:

-   **File System**: Analyzing a digital forensics image (low-level copy) of a system’s storage reveals much information, such as installed programs, created files, partially overwritten files, and deleted files.
-   **System memory**: If the attacker runs their malicious program in memory without saving it to the disk, taking a forensic image (low-level copy) of the system memory is the best way to analyze its contents and learn about the attack.
-   **System logs**: Each client and server computer maintains different log files about what is happening. Log files provide plenty of information about what happened on a system. Even if the attacker tries to clear their traces, some traces will remain.
-   **Network logs**: Logs of the network packets that have traversed a network would help answer more questions about whether an attack is occurring and what it entails.

<small>Also read: [Digital Forensics and Incident Response (DFIR)](https://www.paloaltonetworks.com/cyberpedia/digital-forensics-and-incident-response)</small>

#### Incident Response

An incident usually refers to a data breach or cyber attack; however, in some cases, it can be something less critical, such as a misconfiguration, an intrusion attempt, or a policy violation.

Examples of a cyber attack include an attacker making our network or systems inaccessible, defacing (changing) the public website, and data breach (stealing company data).

How would you respond to a cyber attack? Incident response specifies the methodology that should be followed to handle such a case. The aim is to reduce damage and recover in the shortest time possible. Ideally, you would develop a plan that is ready for incident response.

The four major phases of the incident response process are:

![incident-response](../image/incident-response.png)

-   **Preparation**: This requires a team trained and ready to handle incidents. Ideally, various measures are put in place to prevent incidents from happening in the first place.
-   **Detection and Analysis**: The team has the necessary resources to detect any incident; moreover, it is essential to analyze any detected incident further to learn about its severity.
-   **Containment, Eradication, and Recovery**: Once an incident is detected, it is crucial to stop it from affecting other systems, eliminate it, and recover the affected systems. For instance, when we notice that a system is infected with a computer virus, we would like to stop (contain) the virus from spreading to other systems, clean (eradicate) the virus, and ensure proper system recovery.
-   **Post-Incident Activity**: After a successful recovery, a report is produced, and the lesson learned is shared to prevent similar future incidents.

#### Malware Analysis

> Malware stands for malicious software. Software refers to programs, documents, and files you can save on a disk or send over the network. Malware includes many types, such as:

-   A virus is a piece of code (part of a program) that attaches itself to a program. It is designed to spread from one computer to another and works by altering, overwriting, and deleting files once it infects a computer. The result ranges from the computer becoming slow to unusable.
-   **Trojan Horse** is a program that shows one desirable function but hides a malicious function underneath. For example, a victim might download a video player from a shady website that gives the attacker complete control over their system.
-   **Ransomware** is a malicious program that encrypts the user’s files. Encryption makes the files unreadable without knowing the encryption password. The attacker offers the user the encryption password if the user is willing to pay a “ransom.”

Malware analysis aims to learn about malicious programs using various means:

-   Static analysis works by inspecting the malicious program without running it. This usually requires solid knowledge of assembly language (the processor’s instruction set, i.e., the computer’s fundamental instructions).
-   Dynamic analysis works by running the malware in a controlled environment and monitoring its activities. It lets you observe how the malware behaves when running.

## Careers
