# Web Shell Attacks

Table of Contents

- [Web Shell Attacks](#web-shell-attacks)
- [Overview](#overview)
  - [Web shells as entry point for attacks](#web-shells-as-entry-point-for-attacks)
  - [Web shells as persistence mechanisms](#web-shells-as-persistence-mechanisms)
  - [Challenges in detecting web shells](#challenges-in-detecting-web-shells)
  - [Hardening servers against web shells](#hardening-servers-against-web-shells)
  - [Source](#source)

# Overview

**A web shell** is typically a small piece of malicious code written in typical web development programming languages (e.g., ASP, PHP, JSP) that attackers implant on web servers to provide remote access and code execution to server functions. Web shells allow attackers to run commands on servers to steal data or use the server as launch pad for other activities like credential theft, lateral movement, deployment of additional payloads, or hands-on-keyboard activity, while allowing attackers to persist in an affected organization.

## Web shells as entry point for attacks

Attackers install web shells on servers by taking advantage of security gaps, typically vulnerabilities in web applications, in internet-facing servers. These attackers scan the internet, often using public scanning interfaces like shodan.io, to locate servers to target. They may use previously fixed vulnerabilities that unfortunately remain unpatched in many servers, but they are also known to quickly take advantage of newly disclosed vulnerabilities.

## Web shells as persistence mechanisms

Once installed on a server, web shells serve as one of the most effective means of persistence in an enterprise. We frequently see cases where web shells are used solely as a persistence mechanism. Web shells guarantee that a backdoor exists in a compromised network, because an attacker leaves a malicious implant after establishing an initial foothold on a server. If left undetected, web shells provide a way for attackers to continue to gather data from and monetize the networks that they have access to.

## Challenges in detecting web shells

Web shells can be built using any of several languages that are popular with web applications. Within each language, there are several means of executing arbitrary commands and there are multiple means for arbitrary attacker input. Attackers can also hide instructions in the user agent string or any of the parameters that get passed during a web server/client exchange.

Attackers often compress web shell code into a few bytes, with minimal readable content (e.g., eval), requiring contextual analysis for detection. However, identifying intent is challenging, as some scripts appear harmless until executed. Simple file-upload web shells, which only enable attackers to upload additional malicious files, are particularly hard to detect due to their lightweight nature.

Additionally, web shells can be hidden in non-executable files like media files. If a web server is configured to execute server-side code, a seemingly harmless image can trigger malicious actions when accessed through a browser. These stealthy techniques contribute to the growing use of web shells in cyberattacks.

To counteract this threat, behavior-based detection technologies are being developed to improve protection against web shell attacks.

## Hardening servers against web shells

A single web shell allowing attackers to remotely run commands on a server can have far-reaching consequences. With script-based malware, however, everything eventually funnels to a few natural chokepoints, such as cmd.exe, powershell.exe, and cscript.exe. As with most attack vectors, prevention is critical.

Organizations can harden systems against web shell attacks by taking these preventive steps:

- Identify and remediate vulnerabilities or misconfigurations in web applications and web servers. Use Threat and Vulnerability Management to discover and fix these weaknesses. Deploy the latest security updates as soon as they become available.

- Implement proper segmentation of your perimeter network, such that a compromised web server does not lead to the compromise of the enterprise network.

- Enable antivirus protection on web servers. Turn on cloud-delivered protection to get the latest defenses against new and emerging threats. Users should only be able to upload files in directories that can be scanned by antivirus and configured to not allow server-side scripting or execution.

- Audit and review logs from web servers frequently. Be aware of all systems you expose directly to the internet.

- Utilize the Windows Defender Firewall, intrusion prevention devices, and your network firewall to prevent command-and-control server communication among endpoints whenever possible, limiting lateral movement, as well as other attack activities.

- Check your perimeter firewall and proxy to restrict unnecessary access to services, including access to services through non-standard ports.

- Practice good credential hygiene. Limit the use of accounts with local or domain admin level privileges.

## Source

[Web shell attacks continue to rise - Microsoft](https://www.microsoft.com/en-us/security/blog/2021/02/11/web-shell-attacks-continue-to-rise/)
