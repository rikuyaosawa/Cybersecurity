# Common Attacks

Table of Contents

- [Common Attacks](#common-attacks)
  - [Overview](#overview)
  - [Social Engineering](#social-engineering)
    - [Phishing](#phishing)
  - [Malware](#malware)
    - [Ransomware](#ransomware)
  - [Passwords and Authentication](#passwords-and-authentication)
    - [Exposed Passwords](#exposed-passwords)
    - [Password Attacks](#password-attacks)
  - [Multi-Factor Authentication and Password Managers](#multi-factor-authentication-and-password-managers)
    - [Password Managers and Generating Strong Passwords](#password-managers-and-generating-strong-passwords)
  - [Public Network Safety](#public-network-safety)
    - [Website Connection Security](#website-connection-security)
  - [Backups](#backups)
  - [Updates and Patches](#updates-and-patches)
    - [Antivirus Updates](#antivirus-updates)

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

## Passwords and Authentication

Passwords are central to most authentication systems, protecting everything from social media to banking apps. However, even strong passwords can be undermined by poor practices, like writing them in visible places or reusing them across multiple services.

This guide covers how to create strong passwords and additional steps to enhance authentication security.

**What Makes a Strong Password?**

Previously, strong passwords focused on complexity. For example:
`@Ed1nburgh#1988-2000!` This password mixes uppercase, lowercase, symbols, and numbers, making it resistant to brute-force attacks. However, personal connections (like using familiar names or dates) can make such passwords vulnerable to **social engineering**.

**Current Best Practices:**
Today, the emphasis is on **length over complexity**. Passphrases like:
`Vim is _obviously_, indisputably the best text editor in existence!`
are longer, easier to remember, and harder to crack despite appearing less complex.

**Ideal Approach:**
For maximum security, use long, random strings:
`w41=V1)S7KIJGPN,dII>cHEh>FRVQsj3M^]CB`
While highly secure, these are difficult to remember, but this issue is easily solved with a **password manager**, which will be discussed in the next section.

### Exposed Passwords

If a service is hacked and user account data is leaked, the impact depends on how securely the service stored your information.

- **Best-Case Scenario:**
  If the service used a **secure hashing algorithm** and you have a **strong password**, your password is likely safe. However, your **email address or username** may still be exposed, which could lead to **spam or phishing attempts**.

- **Worst-Case Scenario:**
  If passwords were stored in **plaintext** or with weak hashing, attackers could easily access your login credentials. This allows them to:
  - **Take over your account** on the compromised service.
  - Perform **credential stuffing**—trying your stolen username and password on other sites to exploit password reuse.

Leaked credentials often circulate on the **dark web**, increasing the risk of further attacks.

#### **Protecting Yourself with Data Exposure Notifications**

To stay informed about breaches, use **data exposure notification services** like **[Have I Been Pwned?](https://haveibeenpwned.com/)**. This free service checks if your **email** has appeared in known data breaches and allows you to sign up for **alerts** if future breaches occur.

While not a foolproof defense, these notifications provide an **early warning**, giving you time to **change your passwords** before attackers exploit the breach.

### Password Attacks

An attacker has a few options when it comes to attacking passwords and authentication systems. Some attacks are entirely local (i.e. working entirely on a device owned by the attacker without interacting with the target service at all), others are remote attacks involving the original server.

- **Local attacks** require a stolen copy of the credentials in question. The attacker will take a file full of stolen usernames/emails and hashed passwords, then use software to effectively try to guess the input that created the hash either using randomly generated sequences of characters (slower but more thorough) or by using a pre-generated wordlist of possible passwords (faster but much more likely to miss things). Hybrid types are also very widely used; these are when an attacker takes an existing wordlist and mutates it to add new characters, symbols, or random elements. Local password attacks will be demonstrated in the interactive element for this task.

- **Remote attacks** tend to be one of two categories; they either involve attempting to brute-force known usernames by sending requests to the server and seeing what it responds with, or they use known username and password pairs from previous breaches to see if they are valid on the target site — this is the aforementioned credential stuffing.

## Multi-Factor Authentication and Password Managers

**Multi-Factor Authentication (or MFA)** is a term used to describe any authentication process where you need more than one thing to log in. An example is **a Time-based One Time Password (or TOTP)**, one of the most common second factors currently in use.

Unfortunately, SMS (text message) based TOTP authentication — despite being the most commonly used — is far from the most secure as there have been documented cases of attackers managing to reroute a victim's texts without undue difficulty.

Fortunately, it is possible to generate second-factor authentication yourself, such as using Authenticator APP which requires no network connectivity or interceptable SMS.

### Password Managers and Generating Strong Passwords

At the most basic level, **password managers** provide a safe space to store your passwords. They store passwords in "vaults": encrypted storage either locally on your own device, or as an online service (which also usually allows you to access your passwords from any device). These vaults are accessed using a master password — the only password you need to remember — or (more commonly in recent years) biometric data such as a fingerprint.

## Public Network Safety

Public WiFi, whilst incredibly handy, also gives an attacker ideal opportunities to attack other users' devices or simply intercept and record traffic to steal sensitive information. This latter technique can be as simple as exploiting the fact that most people expect to see public networks available. The attacker can quickly set up a network of their own and monitor the traffic of everyone who connects; this is referred to as a "man-in-the-middle" attack and is very easy to carry out.

The ideal solution to this problem is simply not connecting to untrusted networks. Beneficial though public wireless connections are, it will always be safer to use a mobile hotspot or private network. Unfortunately, the ideal solution is not always feasible; when this is the case, we must rely on other methods of staying safe.

**Virtual Private Networks (VPNs)** encrypt all traffic leaving and re-entering your machine, rendering any interception techniques useless as the intercepted data will simply look like gibberish.

### Website Connection Security

The encrypted connection used to create **HTTPS (Hyper Text Transfer Protocol Secure)** is referred to as **TLS (Transport Layer Security)**, and in most browsers is represented by a padlock to the left of the search bar, which indicates that the connection is secure.

> [!WARNING]
>
> If you are accessing a website without the padlock symbol, **never** enter any credentials or sensitive information — especially if you are using an untrusted network.

## Backups

**Backups** are arguably the single most important defensive measure you can take to protect your data. No matter what happens, if you have taken appropriate steps to back your information up, you will always be able to recover almost regardless of the severity of the damage.

The **3-2-1 backup rule** is a widely recommended strategy for ensuring data safety and disaster recovery. Here's what it means:

**3 Copies of Your Data:**

- Keep **three total copies** of your data. This includes the original data and **two backups**.

**2 Different Storage Media:**

- Store the copies on **at least two different types of storage media**. For example, one copy on your computer’s hard drive and another on an external hard drive or a Network Attached Storage (NAS) device.

**1 Copy Offsite:**

- Keep **one backup copy offsite**. This could be in the cloud or at a physical location different from where the primary data is stored to protect against local disasters (e.g., fire, theft, flood).

#### Why It Matters

- **Redundancy:** Having multiple copies reduces the risk of total data loss.
- **Diverse Media:** Using different storage types protects against specific hardware failures.
- **Offsite Protection:** Ensures data safety from physical threats like natural disasters.

## Updates and Patches

Updates are an essential part of the software development lifecycle; they allow developers to add new features, fix bugs and otherwise simply alter aspects of the product. When vulnerabilities are discovered in software, the developers usually release special updates called patches that contain a fix for the vulnerability or otherwise "patch" the security issue.

For this reason, it is imperative that you update software whenever possible — especially for things like operating systems (e.g. Windows or macOS) where vulnerabilities can be particularly dangerous.

### Antivirus Updates

Most antivirus software packages receive very frequent updates; this is because they largely work using a local database of known exploit signatures, which must be kept up-to-date.

In other words: when new malware is discovered, it gets sent around antivirus vendors who generate a "signature" that identifies this particular piece of malicious software. These signatures are then distributed to every device on the planet that uses the antivirus software, ensuring that your installed antivirus solution is kept up-to-date on all the latest (known) malware.

If antivirus software is not allowed to update it will still be able to catch some malware through other methods. However, the local signature database will quickly become outdated, resulting in malicious software potentially falling through the gaps. In short: if the antivirus wants to update, let it!
