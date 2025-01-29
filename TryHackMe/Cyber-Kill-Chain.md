# Cyber Kill Chain

Table of Contents

- [Cyber Kill Chain](#cyber-kill-chain)
  - [Overview](#overview)
  - [Reconnaissance](#reconnaissance)
    - [Email Harvesting](#email-harvesting)
  - [Weaponization](#weaponization)
    - [Terminology](#terminology)
  - [Delivery](#delivery)
  - [Exploitation](#exploitation)
  - [Installation](#installation)
  - [Command \& Control](#command--control)
  - [Actions on Objectives (Exfiltration)](#actions-on-objectives-exfiltration)

## Overview

The term kill chain is a military concept related to the structure of an attack. It consists of target identification, decision and order to attack the target, and finally the target destruction.

Thanks to **[Lockheed Martin ↗](https://www.lockheedmartin.com/en-us/capabilities/cyber.html)**, a global security and aerospace company, that established the **Cyber Kill Chain®** framework for the cybersecurity industry in 2011 based on the military concept.

The framework defines the steps used by adversaries or malicious actors in cyberspace. To succeed, an adversary needs to go through all phases of the Kill Chain. We will go through the attack phases and help you better understand adversaries and their techniques used in the attack to defend yourself.

The Cyber Kill Chain will help you understand and protect against ransomware attacks, security breaches as well as **Advanced Persistent Threats (APTs)**.

## Reconnaissance

**Reconnaissance** is discovering and collecting information on the system and the victim. The reconnaissance phase is the planning phase for the adversaries.

**OSINT (Open-Source Intelligence)** also falls under reconnaissance. OSINT is the first step an attacker needs to complete to carry out the further phases of an attack. The attacker needs to study the victim by collecting every available piece of information on the company and its employees, such as the company's size, email addresses, phone numbers from publicly available resources to determine the best target for the attack.

> <small>[More on OSINT ↗](https://www.varonis.com/blog/what-is-osint)</small>

### Email Harvesting

**Email harvesting** is the process of obtaining email addresses from public, paid, or free services. An attacker can use email-address harvesting for a **phishing attack** (a type of social-engineering attack used to steal sensitive data, including login credentials and credit card numbers). The attacker will have a big arsenal of tools available for reconnaissance purposes. Here are some of them:

- **theHarvester** - other than gathering emails, this tool is also capable of gathering names, subdomains, IPs, and URLs using multiple public data sources
- **Hunter.io** - this is an email hunting tool that will let you obtain contact information associated with the domain
- **OSINT Framework** - OSINT Framework provides the collection of OSINT tools based on various categories

The information found on social media can also be beneficial for an attacker to conduct a phishing attack.

## Weaponization

After a successful reconnaissance stage, the attacker would work on crafting a "weapon of destruction". He would prefer not to interact with the victim directly and, instead, he will create a **"weaponizer"** that, according to Lockheed Martin, combines malware and exploit into a deliverable payload.

Most attackers usually use automated tools to generate the malware or refer to the [DarkWeb ↗](https://www.kaspersky.com/resource-center/threats/deep-web) to purchase the malware. More sophisticated actors or nation-sponsored APT (Advanced Persistent Threat Groups) would write their custom malware to make the malware sample unique and evade detection on the target.

### Terminology

- **Malware** is a program or software that is designed to damage, disrupt, or gain unauthorized access to a computer.
- An **exploit** is a program or a code that takes advantage of the vulnerability or flaw in the application or system.
- A **payload** is a malicious code that the attacker runs on the system.

In the Weaponization phase, the attacker would:

- Create an infected Microsoft Office document containing a malicious macro or VBA (Visual Basic for Applications) scripts.
- An attacker can create a malicious payload or a very sophisticated worm, implant it on the USB drives, and then distribute them in public. An example of the virus.
- An attacker would choose Command and Control (C2) techniques for executing the commands on the victim's machine or deliver more payloads.
- An attacker would select a backdoor implant (the way to access the computer system, which includes bypassing the security mechanisms).

## Delivery

The **Delivery** phase is when the attacker decides to choose the method for transmitting the payload or the malware. He has plenty of options to choose from:

- **Phishing email**: after conducting the reconnaissance and determining the targets for the attack, the malicious actor would craft a malicious email that would target either a specific person (spearphishing attack) or multiple people in the company. The email would contain a payload or malware.

- **Distributing infected USB drives** in public places like coffee shops, parking lots, or on the street. An attacker might decide to conduct a sophisticated USB Drop Attack by printing the company's logo on the USB drives and mailing them to the company while pretending to be a customer sending the USB devices as a gift.

- **Watering hole attack**: a targeted attack designed to aim at a specific group of people by compromising the website they are usually visiting and then redirecting them to the malicious website of an attacker's choice. The attacker would look for a known vulnerability for the website and try to exploit it. The attacker would encourage the victims to visit the website by sending "harmless" emails pointing out the malicious URL to make the attack work more efficiently. After visiting the website, the victim would unintentionally download malware or a malicious application to their computer. This type of attack is called a **drive-by download**.

## Exploitation

To gain access to the system, an attacker needs to exploit the vulnerability.

After gaining access to the system, the malicious actor could exploit software, system, or server-based vulnerabilities to escalate the privileges or move laterally through the network. According to CrowdStrike, **lateral movement** refers to the techniques that a malicious actor uses after gaining initial access to the victim's machine to move deeper into a network to obtain sensitive data.

The attacker might also apply a **"Zero-day Exploit"** in this stage. According to FireEye, "the zero-day exploit or a zero-day vulnerability is an unknown exploit in the wild that exposes a vulnerability in software or hardware and can create complicated problems well before anyone realizes something is wrong. A zero-day exploit leaves NO opportunity for detection at the beginning."

## Installation

Once the attacker gets access to the system, he would want to reaccess the system if he loses the connection to it or if he got detected and got the initial access removed, or if the system is later patched. He will no longer have access to it.

That is when the attacker needs to install a **persistent backdoor**. A persistent backdoor will let the attacker access the system he compromised in the past.

The persistence can be achieved through:

- **Installing a web shell on the webserver**. A web shell is a malicious script written in web development programming languages such as ASP, PHP, or JSP used by an attacker to maintain access to the compromised system. Because of the web shell simplicity and file formatting (.php, .asp, .aspx, .jsp, etc.) can be difficult to detect and might be classified as benign.

  > <small>[More on web shell (auxiliary note)](../auxiliary-notes/Web-Shell-Attacks.md)</small>

- **Installing a backdoor on the victim's machine**. For example, the attacker can use Meterpreter to install a backdoor on the victim's machine. Meterpreter is a Metasploit Framework payload that gives an interactive shell from which an attacker can interact with the victim's machine remotely and execute the malicious code.

- **Creating or modifying Windows services**. This technique is known as T1543.003 on MITRE ATT&CK (MITRE ATT&CK® is a knowledge base of adversary tactics and techniques based on real-world scenarios). An attacker can create or modify the Windows services to execute the malicious scripts or payloads regularly as a part of the persistence. An attacker can use the tools like sc.exe (sc.exe lets you Create, Start, Stop, Query, or Delete any Windows Service) and Reg to modify service configurations. The attacker can also masquerade the malicious payload by using a service name that is known to be related to the Operating System or legitimate software.

- **Adding the entry to the "run keys" for the malicious payload in the Registry or the Startup Folder**. By doing that, the payload will execute each time the user logs in on the computer. According to MITRE ATT&CK, there is a startup folder location for individual user accounts and a system-wide startup folder that will be checked no matter what user account logs in.

In this phase, the attacker can also use the **Timestomping** technique to avoid detection by the forensic investigator and also to make the malware appear as a part of a legitimate program. The Timestomping technique lets an attacker modify the file's timestamps, including the modify, access, create and change times.

## Command & Control

After getting persistence and executing the malware on the victim's machine, the attacker opens up the **C2 (Command and Control) channel through the malware to remotely control and manipulate the victim**. This term is also known as **C&C or C2 Beaconing** as a type of malicious communication between a C&C server and malware on the infected host. The infected host will consistently communicate with the C2 server; that is also where the beaconing term came from.

The compromised endpoint would communicate with an external server set up by an attacker to establish a command & control channel. After establishing the connection, the attacker has full control of the victim's machine. Until recently, IRC (Internet Relay Chat) was the traditional C2 channel used by attackers. This is no longer the case, as modern security solutions can easily detect malicious IRC traffic.

The most common C2 channels used by adversaries nowadays:

- **The protocols HTTP on port 80 and HTTPS on port 443** - this type of beaconing blends the malicious traffic with the legitimate traffic and can help the attacker evade firewalls.
- **DNS (Domain Name Server)**. The infected machine makes constant DNS requests to the DNS server that belongs to an attacker, this type of C2 communication is also known as **DNS Tunneling**.

Important to note that an adversary or another compromised host can be the owner of the C2 infrastructure.

## Actions on Objectives (Exfiltration)

After going through six phases of the attack, the attacker can finally achieve his goals, which means taking action on the original objectives. With hands-on keyboard access, the attacker can achieve the following:

- Collect the credentials from users.
- Perform privilege escalation (gaining elevated access like domain administrator access from a workstation by exploiting the misconfiguration).
- Internal reconnaissance (for example, an attacker gets to interact with internal software to find its vulnerabilities).
- Lateral movement through the company's environment.
- Collect and exfiltrate sensitive data.
- Deleting the backups and shadow copies. Shadow Copy is a Microsoft technology that can create backup copies, snapshots of computer files, or volumes.
- Overwrite or corrupt data.

---

End
