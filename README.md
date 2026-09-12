# Departmental Network Segmentation and Access Control

This project demonstrates the design and configuration of a departmental network using **Cisco Packet Tracer**. The network connects IT, Sales, and HR departments while using an **Access Control List (ACL)** to control communication between departments and maintain access to required network services.

## Table of Contents

* Project Overview
* Network Topology
* Tools and Technologies
* Configuration Steps
* Results and Findings
* Author

## Project Overview

The purpose of this project was to build a functional network for three organizational departments: **IT, Sales, and HR**. The project involved configuring network devices, assigning departmental IP addressing, testing connectivity, and implementing an **ACL** to restrict specific network traffic.

The configuration demonstrates fundamental networking and security concepts, including **network segmentation, IP addressing, routing, connectivity testing, and access control**.

## Network Topology

The network topology consists of:

* **1 Cisco 2911 Router**
* **3 Cisco 2960 Switches**
* **6 PCs**, with two PCs assigned to each department
* **1 Server** located within the IT department
* Three departmental networks:

  * **IT Department:** `192.168.10.0/24`
  * **Sales Department:** `192.168.20.0/24`
  * **HR Department:** `192.168.30.0/24`
* Default gateways:

  * **IT:** `192.168.10.1`
  * **Sales:** `192.168.20.1`
  * **HR:** `192.168.30.1`

Each department is connected to its own switch, while the switches connect through the router to enable communication between the departmental networks.

## Tools and Technologies

* **Cisco Packet Tracer**
* **Cisco 2911 Router**
* **Cisco 2960 Switches**
* **PC End Devices**
* **Server**
* **IPv4 Addressing**
* **Subnetting**
* **Router CLI**
* **Access Control Lists (ACLs)**
* **ICMP / Ping Testing**
* **HTTP Service**

## Configuration Steps

1. Created the network topology in **Cisco Packet Tracer** using one Cisco 2911 router, three Cisco 2960 switches, six PCs, and one server.

2. Organized the network into three departments: **IT, Sales, and HR**, with two PCs assigned to each department and the server located within the IT network.

3. Configured the departmental IPv4 networks as `192.168.10.0/24`, `192.168.20.0/24`, and `192.168.30.0/24`.

4. Configured the appropriate IP addresses, subnet masks, and default gateways on the network devices.

5. Tested communication between departments using the `ping` command.

6. Verified successful connectivity from an **HR department PC** to an **IT department PC**.

7. Configured an **extended ACL** through the router CLI to deny ICMP traffic from the Sales network to the IT network while permitting other IP traffic.

8. Applied the ACL to the appropriate router interface using the `ip access-group` command.

9. Tested the ACL by attempting to `ping` an IT PC from a Sales PC and confirmed that the communication was blocked.

10. Verified that the **Sales department retained access to the HTTP service** hosted on the server despite the ICMP restriction.

## Results and Findings

The completed network successfully demonstrated communication and controlled access between multiple organizational departments.

* **HR-to-IT connectivity was successful**, confirming that routing between the departmental networks was functioning correctly.
* **Sales-to-IT ICMP traffic was successfully blocked** after the ACL was implemented.
* The failed Sales-to-IT `ping` confirmed that the configured access-control rule was being enforced.
* **Sales retained access to the server's HTTP service**, demonstrating that access could be restricted selectively without unnecessarily blocking legitimate network services.
* The project demonstrated practical implementation of **network segmentation, routing, IP configuration, connectivity testing, and ACL-based traffic control**.

## Author

**Concord Ekwonna**

* **Field:** Governance, Risk, and Compliance (GRC)
* **Location:** Canada
* **Email:** [concordekwonna@gmail.com](mailto:concordekwonna@gmail.com)
