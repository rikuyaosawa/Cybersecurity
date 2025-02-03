# Common Attacks

Table of Contents

- [Common Attacks](#common-attacks)
  - [Overview](#overview)
  - [Social Engineering](#social-engineering)
    - [Phishing](#phishing)
  - [Malware](#malware)
    - [Ransomware](#ransomware)

## Overview

Our existence in a digital world makes it imperative that we understand and can protect against common attacks.

We shall discuss following common attacks:

- Social Engineering and Phishing
- Malware and Ransomware
- Password and Authentication

and a few methods to stay safe:

- Multi-Factor Authentication and Password Managers
- Public Network Safety
- Backups
- Updates and Patches

## Social Engineering

**Social Engineering** is the term used to describe any cyberattack where a human (rather than a computer) is the target; for this reason, it is sometimes referred to as "People Hacking". For example, if an attacker wishes to obtain a victim's password, they could attempt to guess or brute-force the password — or they could simply ask you.

Charismatic hackers calling your phone company and taking possession of your account is one form of social engineering; however, there are many other types. Social engineering is a vast topic, encompassing any attack that relies on tricking humans into giving the attacker access, rather than attacking the technology directly.

Whilst direct interaction with targets is the most common style of social engineering, other examples include dropping USB storage devices in public (e.g. in company car parks) in the hope that someone (often a company employee) will pick one up and plug it into a sensitive computer. In a similar vein, attackers may leave a "charging cable" plugged into a socket in a public place. In actuality, the cable contains malicious software such as keyloggers or tools to take control of the victim's device.

#### Staying Safe from Social Engineering Attacks

In many ways, it is very tricky to stay safe from social engineering as it won't always be you who the attacker is talking to, but rather someone who can give them what they need without your consent (e.g. calling your bank whilst pretending to be you, so as to access your bank account). That said, there are still measures you can take to protect yourself from Social Engineering attacks:

- **Always make sure to set up multiple forms of authentication, and ensure that providers respect these.** For example, set difficult to guess — or otherwise incorrect — answers to security questions (making sure to store the answers somewhere safe!), and make sure that these questions are asked when you try to access accounts over the phone.

- **Never plug external media (e.g. USBs/CDs/etc) into a computer that you care about or that is connected to any other devices.** Ideally, don't plug the media in at all, and instead give it to your local police for safekeeping.

- **Always insist on proof of identity when a stranger calls or messages you claiming to work for a company whose services you use.** Where possible, confirm with a known phone number or email address that the call or message you received was legitimate (i.e. use a trusted method to get in contact with the company to confirm). Remember that no legitimate employee will ever ask for your password or other information that protects your account.

### Phishing

**Phishing** is one of the most common cyber attack types employed by scammers and bad actors, targeting individuals and businesses indiscriminately.

In many cases, phishing is the initial attack vector used to gain access to a company's infrastructure before performing further attacks against the corporate network. Whilst there are many automated tools now available to help combat phishing threats, phishing is still one of the most prolific attack vectors around.

Phishing is a sub-section of social engineering. Whereas social engineering is a very general term used to describe any attack that takes advantage of a human rather than a computer system, phishing specifically describes attacks whereby a scammer or other attacker tricks a victim into opening a malicious webpage by sending them a text message, email, or another form of online correspondence.

There are three primary types of phishing attacks:

| **Attack Type**      | **Definition**                                                                                                                                                                                                                                                |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **General Phishing** | A simple, mass phishing attack targeting large groups (e.g., PayPal or Amazon users). These campaigns are usually basic, often containing poorly crafted messages and malicious sites with visible errors, making them relatively easy to identify.           |
| **Spearphishing**    | A more targeted attack aimed at specific individuals or groups (e.g., employees of a company). Spearphishing campaigns are better crafted than general phishing, with messages and malicious sites tailored to the target, often as part of larger campaigns. |
| **Whaling**          | A highly specific attack targeting high-value individuals (e.g., C-suite executives). Whaling messages are extremely well crafted, sophisticated, and difficult to detect due to their professional appearance and tailored content.                          |

#### Staying Safe from Phishing Attacks

There are a variety of things that you can (and should!) do to keep yourself safe from phishing attacks:

- **Delete unknown or untrusted emails without opening them.** If you can see anything suspicious in the email, also report it as spam to your email provider, or forward it to your IT Security department if you received the email at work.
- **Never open attachments from untrusted emails** — this includes any attachments from a legitimate contact that you were not expecting.
- **Do not click on embedded links in emails or messages.** Where possible, navigate to the real website in your web browser and access the content that way. If you absolutely must click on the link, ensure that the domain name is correct and that the link points to where you think it does.
- **Always make sure that your device and antivirus software are up-to-date.**
- **Avoid making your personal information (e.g. email address and phone number) public if possible.** If you must publish personal details publicly, create a "burner" email address (a temporary address made for one purpose, then destroyed soon afterwards) for the occasion, then destroy it as soon as it is no longer required.

## Malware

Despite the steady advance of antivirus software solutions, malware (and ransomware in particular) is an ever-growing threat.

**Malware** (short for "malicious software") can be defined as any software designed to perform malicious actions on behalf of an attacker. There are many different kinds of malware: we will be focussing on generic malware and ransomware specifically in this task.

Once installed, attackers commonly use malware to steal information, cause damage, or execute arbitrary commands on the infected system. Malware is often used to perform a set of tasks referred to as **"Command and Control"** (or C2/C&C). C2 malware connects back to a waiting server and allows an attacker to control the infected system remotely, often incorporating many simple tasks such as keylogging as built-in parts of the malicious software.

### Ransomware

A specialised class of malware: **ransomware** is used to infect as many systems as possible, encrypting the data on the devices and holding it to ransom. If the victims pay the attackers within a set timeframe (usually via a cryptocurrency such as Bitcoin), the data is theoretically returned.

Ransomware usually spreads by exploiting known vulnerabilities in commonly installed software (e.g. the Microsoft Windows operating system); it can be extremely fast-spreading once an infection begins, and can demand millions in ransom money. The goal of a ransomware attack is to infect as many systems as possible, then make as much data inaccessible as possible by encrypting it with a key known only to the attacker.

#### Common Methods of Malware Infection

**1. Email-Based Malware Delivery**

Attackers may send emails with malicious attachments, such as:

- **Microsoft Word/Excel Files:** Contain malicious macros that execute when the user clicks **"Enable Content"**.
- **Executable Files (.exe):** Compiled programs designed to run malicious code.
- **PDF Files:** Exploiting vulnerabilities in PDF readers.
- **PowerShell Scripts (.ps1):** Scripts executed via PowerShell, capable of automating malicious tasks.
- **Batch Scripts (.bat):** Simple command-line scripts to execute malicious commands.
- **HTML Application Files (.hta):** Can run scripts with higher privileges.
- **JavaScript Files (.js):** Executed by Windows’ built-in JavaScript interpreter.

**2. Exploiting Vulnerabilities in Public-Facing Systems**

Attackers can target:

- **Web Servers**
- **Network Devices**
- **Corporate Infrastructure**

By exploiting vulnerabilities, attackers gain unauthorized access to internal networks, using malware to escalate the attack further.

#### Staying Safe from Malware

- Always accept updates and patches when offered — especially in important software like operating systems. Updates often contain fixes to security flaws, so it is important to get these in place as soon as possible.
- Never click on suspicious links, especially in emails. Try not to open file attachments if possible. If a message looks suspicious, delete it, or forward it to the appropriate team if using your work account.
- Always be on the lookout for people trying to get you to download or run files — especially over email or instant messaging.
- Never plug unknown media devices (e.g. USB devices) into important computers. If you find a device in public, do not plug it into your work laptop!
- Always back up important data — this will be discussed in more detail later in the room and can be crucial in recovering from a ransomware attack.
- Make sure that your antivirus software is always up-to-date and activated.
