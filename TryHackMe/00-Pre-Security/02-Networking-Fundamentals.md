# Networking FUndamentals

Table of Contents

- [Networking FUndamentals](#networking-fundamentals)
  - [What is Networking?](#what-is-networking)
  - [What is the Internet?](#what-is-the-internet)
  - [Identifying Devices on a Network](#identifying-devices-on-a-network)
    - [IP Addresses](#ip-addresses)
    - [MAC Addresses](#mac-addresses)
    - [Spoofing](#spoofing)
  - [Ping (ICMP)](#ping-icmp)

## What is Networking?

In computing, a **network** is simply devices that are connected together. A network can be formed by anywhere from 2 devices to billions. These devices include everything from your laptop and phone to security cameras, traffic lights and even farming!

Networks are integrated into our everyday life. Be it gathering data for the weather, delivering electricity to homes or even determining who has the right of way at a road. Because networks are so embedded in the modern-day, networking is an essential concept to grasp in cybersecurity.

## What is the Internet?

**The Internet** is one giant network that consists of many, many small networks within itself.

The first iteration of the Internet was within the ARPANET project in the late 1960s. This project was funded by the United States Defence Department and was the first documented network in action.

However, it wasn't until 1989 when the Internet as we know it was invented by Tim Berners-Lee by the creation of **the World Wide Web (WWW)**. It wasn't until this point that the Internet started to be used as a repository for storing and sharing information, just like it is today.

A network can be one of two types:

- A private network
- A public network

## Identifying Devices on a Network

Every human has an individual set of fingerprints which means that even if they change their name, there is still an identity behind it. Devices have the same thing: two means of identification, with one being permeable.

These are:

- **An IP Address**
- **A Media Access Control (MAC) Address** - think of this as being similar to a serial number.

### IP Addresses

**An IP address (or Internet Protocol)** address can be used as a way of identifying a host on a network for a period of time, where that IP address can then be associated with another device without the IP address changing.

Example of IPv4:

```
192.168.1.1
```

An IP address is a set of numbers that are divided into four **octets**. The value of each octet will summarise to be the IP address of the device on the network. This number is calculated through a technique known as IP addressing & subnetting.

We should recall that devices can be on both a private and public network. Depending on where they are will determine what type of IP address they have: a public or private IP address.

#### Public and Private Address

**A public address is used to identify the device on the Internet, whereas a private address is used to identify a device amongst other devices.** Devices will be able to use their private IP addresses to communicate with each other. However, any data sent to the Internet from either of these devices will be identified by the same public IP address. Public IP addresses are given by your Internet Service Provider (or ISP) at a monthly fee (your bill!)

As more and more devices become connected, it is becoming increasingly harder to get a public address that isn't already in use.

#### IP Address Versions

Enter IP address versions. So far, we have only discussed one version of the Internet Protocol addressing scheme known as **IPv4**, which uses a numbering system of `2^32` IP addresses (4.29 billion).

**IPv6** is a new iteration of the Internet Protocol addressing scheme to help tackle this issue. Although it is seemingly more daunting, it boasts a few benefits:

- Supports up to `2^128` of IP addresses (340 trillion-plus), resolving the issues faced with IPv4
- More efficient due to new methodologies

Example of IPv6:

```
2001:0000:130F:0000:0000:09C0:876A:130B
```

### MAC Addresses

Devices on a network will all have a physical network interface, which is a microchip board found on the device's motherboard. This network interface is assigned a unique address at the factory it was built at, called a **MAC (Media Access Control ) address**.

The MAC address is a **twelve-character** hexadecimal number (a base sixteen numbering system used in computing to represent numbers) split into two's and separated by a colon. These colons are considered separators.

For example,

```
a4:c3:f0:85:ac:2d
```

The first six characters represent the company that made the network interface, and the last six is a unique number.

### Spoofing

However, an interesting thing with MAC addresses is that they can be faked or **"spoofed"** in a process known as **spoofing**. This spoofing occurs when a networked device pretends to identify as another using its MAC address. When this occurs, it can often break poorly implemented security designs that assume that devices talking on a network are trustworthy.

## Ping (ICMP)

**Ping** is one of the most fundamental network tools available to us.

Ping uses **ICMP (Internet Control Message Protocol)** packets to determine the performance of a connection between devices, for example, if the connection exists or is reliable.

The time taken for ICMP packets traveling between devices is measured by ping. This measuring is done using ICMP's echo packet and then ICMP's echo reply from the target device.

Pings can be performed against devices on a network, such as your home network or resources like websites. This tool can be easily used and comes installed on Operating Systems (OSs) such as Linux and Windows. The syntax to do a simple ping is: `ping IP address or website URL`.
