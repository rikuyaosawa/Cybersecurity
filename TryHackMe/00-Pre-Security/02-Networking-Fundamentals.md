# Networking Fundamentals

- [Networking Fundamentals](#networking-fundamentals)
  - [What is Networking?](#what-is-networking)
  - [What is the Internet?](#what-is-the-internet)
  - [Identifying Devices on a Network](#identifying-devices-on-a-network)
    - [IP Addresses](#ip-addresses)
    - [MAC Addresses](#mac-addresses)
    - [Spoofing](#spoofing)
  - [Ping (ICMP)](#ping-icmp)
  - [Intro to LAN](#intro-to-lan)
    - [Star Topology](#star-topology)
    - [Bus Topology](#bus-topology)
    - [Ring Topology](#ring-topology)
    - [What is a Switch?](#what-is-a-switch)
    - [What is a Router?](#what-is-a-router)
    - [A Primer on Subnetting](#a-primer-on-subnetting)
    - [Address Resolution Protocol](#address-resolution-protocol)
    - [Dynamic Host Configuration Protocol](#dynamic-host-configuration-protocol)

## What is Networking?

In computing, a **network** is simply devices that are connected together. These devices include everything from your laptop and phone to security cameras, traffic lights and even farming!

## What is the Internet?

**The Internet** is one giant network that consists of many, many small networks within itself.

The Internet as we know it was invented by Tim Berners-Lee by the creation of **the World Wide Web (WWW)**.

A network can be one of two types:

- A private network
- A public network

## Identifying Devices on a Network

Devices have two means of identification, with one being permeable.

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

Depending on where they are will determine what type of IP address they have: a public or private IP address.

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

## Intro to LAN

Over the years, there has been experimentation and implementation of various network designs. In reference to networking, the term "**topology**" refers to the design or look of the network at hand.

### Star Topology

The main premise of a star topology is that devices are individually connected via a central networking device such as a switch or hub. This topology is the most commonly found today because of its reliability and scalability - despite the cost.

Any information sent to a device in this topology is sent via the central device to which it connects.

**Advantage**

- Scalable in nature, which means that it is very easy to add more devices as the demand for the network increases.

**Disadvantages**

- More expensive than any other topologies because more cabling and the purchase of dedicated networking equipment is required for this topology.

- Prone to failure: If the centralised hardware that connects devices fails, these devices will no longer be able to send or receive data. Thankfully, these centralised hardware devices are often robust.

### Bus Topology

This type of connection relies upon a single connection which is known as a backbone cable. This type of topology is similar to the leaf off of a tree in the sense that devices (leaves) stem from where the branches are on this cable.

**Advantage**

- Cost-efficient: One of the easier and more cost-efficient topologies to set up because of their expenses, such as cabling or dedicated networking equipment used to connect these devices.

**Disadvantages**

- Prone to becoming slow: Because all data destined for each device travels along the same cable, it is very quickly prone to becoming slow and bottlenecked if devices within the topology are simultaneously requesting data.

- Hard to troubleshoot: It gets very difficult troubleshooting when identifying which device is experiencing issues with data all traveling along the same route.

- Little redundancy: There is little redundancy in place in case of failures. This disadvantage is because there is a single point of failure along the backbone cable. If this cable were to break, devices can no longer receive or transmit data along the bus.

### Ring Topology

In the ring topology (also known as token topology), devices such as computers are connected directly to each other to form a loop. It works by sending data across the loop until it reaches the destined device, using other devices along the loop to forward the data.

A device will only send received data from another device in this topology if it does not have any to send itself.

**Advantages**

- Easy to troubleshoot: Because there is only one direction for data to travel across this topology, it is fairly easy to troubleshoot any faults that arise.

- Less prone to bottlenecks as large amounts of traffic are not traveling across the network at any one time.

**Disadvantages**

- Not the most efficient as it may have to visit many multiple devices first before reaching the intended device.

- Little redundancy: the design of this topology does mean that a fault such as cut cable, or broken device will result in the entire networking breaking.

### What is a Switch?

Switches are dedicated devices within a network that are designed to aggregate multiple other devices such as computers, printers, or any other networking-capable device using ethernet. These various devices plug into a switch's port. Switches can connect a large number of devices by having ports of 4, 8, 16, 24, 32, and 64 for devices to plug into.

Switches are much more efficient than their lesser counterpart (hubs/repeaters). Switches keep track of what device is connected to which port. This way, when they receive a packet, instead of repeating that packet to every port like a hub would do, it just sends it to the intended target, thus reducing network traffic.

Both Switches and Routers can be connected to one another. The ability to do this increases the redundancy (the reliability) of a network by adding multiple paths for data to take. If one path goes down, another can be used. Whilst this may reduce the overall performance of a network because packets have to take longer to travel, there is no downtime -- a small price to pay considering the alternative.

### What is a Router?

It's a router's job to connect networks and pass data between them. It does this by using routing.

Routing is the label given to the process of data traveling across networks. Routing involves creating a path between networks so that this data can be successfully delivered.

### A Primer on Subnetting

**Subnetting** is the term given to splitting up a network into smaller, miniature networks within itself. It is achieved by splitting up the number of hosts that can fit within the network, represented by a number called a **subnet mask**.

Subnets use IP addresses in three different ways:

- Identify the network address
- Identify the host address
- Identify the default gateway

### Address Resolution Protocol

The **Address Resolution Protocol or ARP** for short, is the technology that is responsible for allowing devices to identify themselves on a network.

When devices wish to communicate with another, they will send a broadcast to the entire network searching for the specific device. Devices can use ARP to find the MAC address (and therefore the physical identifier) of a device for communication.

In order to map these two identifiers together (IP address and MAC address), ARP sends two types of messages:

- **ARP Request**
- **ARP Reply**

When an ARP request is sent, a message is broadcasted on the network to other devices asking, "What is the mac address that owns this IP address?" When the other devices receive that message, they will only respond if they own that IP address and will send an ARP reply with its MAC address. The requesting device can now remember this mapping and store it in its **ARP cache** for future use.

### Dynamic Host Configuration Protocol

IP addresses can be assigned either manually, by entering them physically into a device, or automatically and most commonly by using a **DHCP (Dynamic Host Configuration Protocol)** server.

1. DHCP Discover: When a device connects to a network, if it has not already been manually assigned an IP address, it sends out a request (DHCP Discover) to see if any DHCP servers are on the network.

2. DHCP Offer: The DHCP server then replies back with an IP address the device could use (DHCP Offer).

3. DHCP Request: The device then sends a reply confirming it wants the offered IP Address (DHCP Request).

4. DHCP ACK: Lastly, the DHCP server sends a reply acknowledging this has been completed, and the device can start using the IP Address (DHCP ACK).
