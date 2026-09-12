# Kali Linux System Information and Network Connectivity Testing

This project demonstrates the use of **Kali Linux command-line tools** to examine system information and perform basic network connectivity tests. It covers system identification, hardware and operating system inspection, IP connectivity testing, domain-name resolution, packet transmission, and network response analysis.

## Table of Contents

* Project Overview
* Network Topology
* Tools and Technologies
* Configuration Steps
* Results and Findings
* Author

## Project Overview

The purpose of this project was to develop practical familiarity with the **Kali Linux command-line environment** and fundamental network troubleshooting techniques.

The project involved identifying system and operating environment information using Linux commands, examining available memory and disk resources, and testing network connectivity by sending **ICMP echo requests** to a known IP address and a domain name.

## Network Topology

This project was completed within a **Kali Linux virtual machine** connected to an external network.

The testing environment included:

* **Kali Linux Virtual Machine**
* Username: `kali`
* Hostname: `kali`
* Current working directory: `/home/kali`
* Approximately **1.91 GiB RAM**
* Approximately **59 GB available disk space** on the main disk partition
* Linux kernel version: `6.19.14+kali-amd64`
* External connectivity test target: `8.8.8.8`
* Domain connectivity test target: `google.com`

Unlike a simulated multi-device network topology, this lab focused on examining the local Kali Linux environment and testing its ability to communicate with external network destinations.

## Tools and Technologies

* **Kali Linux**
* **Linux Terminal / Command Line Interface (CLI)**
* **Virtual Machine**
* **ICMP**
* **DNS Resolution**

## Configuration Steps

1. Opened the **Kali Linux terminal** to begin examining the virtual machine environment.

2. Executed `whoami` to identify the current user and confirmed the username as `kali`.

3. Executed `hostname` to identify the system hostname and confirmed it as `kali`.

4. Used `pwd` to determine the present working directory, which returned `/home/kali`.

5. Executed `free -h` to inspect the virtual machine's memory and identified approximately **1.91 GiB of total RAM**.

6. Used `df -h` to inspect disk utilization and identified approximately **59 GB of available space** on the main disk partition.

7. Executed `uname -a` to obtain operating system and kernel information. The running Linux kernel was identified as `6.19.14+kali-amd64`.

8. Tested basic IP connectivity using `ping -c 2 8.8.8.8`.

9. Reviewed the ping results and confirmed that all transmitted packets were successfully received with **0% packet loss** and an average round-trip time of approximately **26.494 ms**.

10. Tested connectivity to a domain name using `ping -c 4 google.com`.

11. Observed that `google.com` successfully resolved to an IP address and responded to the ICMP requests.

12. Compared the round-trip times between the direct IP-address test and the domain-name test to examine differences in network response times.

## Results and Findings

The project successfully demonstrated the use of fundamental **Linux system administration and network troubleshooting techniques**.

* The system username and hostname were successfully identified as `kali`.
* The current working directory was confirmed as `/home/kali`.
* The Kali Linux VM had approximately **1.91 GiB of RAM**.
* The main disk partition had approximately **59 GB of available space**.
* The running Linux kernel was identified as `6.19.14+kali-amd64`.
* The connectivity test to `8.8.8.8` recorded **0% packet loss**, confirming that the Kali Linux VM had external network connectivity.
* The average round-trip time to `8.8.8.8` was approximately **26.494 ms**.
* The `google.com` test demonstrated successful **domain-name resolution and network communication**.
* The domain-name test showed a higher average round-trip time than the direct IP test.
* The `-c 4` option limited the `ping` command to four packets before terminating automatically.

## Author

**Concord Ekwonna**

* **Field:** Governance, Risk, and Compliance (GRC)
* **Location:** Canada
* **Email:** [concordekwonna@gmail.com](mailto:concordekwonna@gmail.com)
