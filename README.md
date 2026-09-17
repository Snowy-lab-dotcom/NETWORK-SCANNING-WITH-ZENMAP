# 🔎 Network Scanning with Zenmap

![Cybersecurity](https://img.shields.io/badge/Field-Cybersecurity-red)
![Tool](https://img.shields.io/badge/Tool-Zenmap%20%2F%20Nmap-blue)
![Project](https://img.shields.io/badge/Project-Network%20Scanning-green)
![Learning](https://img.shields.io/badge/Purpose-Educational-orange)

## 📌 Project Overview

This project focuses on **network scanning and host discovery using Zenmap**, the graphical user interface for Nmap.

The purpose of this lab is to understand how a cybersecurity professional can identify devices that are active on a local network, determine their IP addresses and MAC addresses, and visualise the discovered network using Zenmap's topology feature.

This project was completed as part of my practical cybersecurity and ethical hacking learning journey.

> ⚠️ **Ethical Use:** Network scanning should only be performed on networks and systems that you own or have explicit permission to test.

---

## 🎯 Project Objectives

The main objectives of this project are to:

* Install Zenmap on a Windows PC.
* Identify the computer's local IP address.
* Identify the local LAN subnet.
* Discover live hosts on the local subnet.
* Determine the number of live hosts.
* Identify the IP addresses of discovered hosts.
* Identify the MAC addresses of discovered hosts.
* Generate and save a network topology diagram as a PDF.
* Problems encoutered.
* Document the practical results and lessons learned.

The project instructions specifically use a `10.0.0.0/24` subnet.

---

# 🛠️ Tools & Technologies

| Tool              | Purpose                                   |
| ----------------- | ----------------------------------------- |
| 🖥️ Windows PC    | Host operating system                     |
| 🔎 Zenmap         | Graphical network scanning interface      |
| 🌐 Nmap           | Network discovery and scanning engine     |
| 💻 Command Prompt | Finding local network information         |
| 📄 PDF            | Saving the network topology               |
| 🐙 GitHub         | Project documentation and version control |

---

# 🧩 Lab Tasks

## Task 1 – Install Zenmap

Zenmap is the official graphical interface for Nmap. It provides a beginner-friendly interface while still supporting advanced Nmap functionality.

The first step was to download Zenmap/Nmap from the official Nmap website and install it on the Windows PC.


### Installation Process

1. Download the Nmap/Zenmap package.<br/>
   <img width="965" height="601" alt="nmap setup" src="https://github.com/user-attachments/assets/13e9d295-bcf0-477f-8c58-4477221ce55d" />

3. Run the installation file.<br/>
   <img width="505" height="387" alt="nmp installing" src="https://github.com/user-attachments/assets/0ad8008f-9614-480a-864e-1a71f0ed7c76" />

5. Follow the installation wizard.<br/>
   <img width="500" height="383" alt="nmap install location" src="https://github.com/user-attachments/assets/5a4ee7e8-b71f-4a39-811c-9e03f29dabc2" />

7. Complete the installation.<br/>
   <img width="527" height="389" alt="nmap agreement" src="https://github.com/user-attachments/assets/8365bc09-c323-4b29-aa79-686bfb234b07" />

9. Open Zenmap.<br/>
<img width="1302" height="643" alt="image" src="https://github.com/user-attachments/assets/236651bd-deba-46e4-8370-2a05bff8ec61" />

---

# 🌐 Task 2 – Find Local IP Address & LAN Subnet

The Windows Command Prompt was used to identify the local network configuration.

The following command was used:

```cmd
ipconfig
```

This command was used to identify:

* IPv4 Address: 192.168.8.253
* Subnet Mask: 255.255.255.0
* Default Gateway: 192.168.8.1
<br/>
<img width="1351" height="758" alt="ipconfig " src="https://github.com/user-attachments/assets/3d5c80ac-3e0b-4689-ac13-3f3879d8556b" />

---

# 🔎 Task 3 – Discover Live Hosts

Zenmap was used to perform a **Ping Scan** against the local LAN subnet.

The local subnet was entered into Zenmap and the **Ping Scan** profile was selected to identify hosts that were responding on the network.

### Scan Configuration

```text
Target: 192.168.8.0/24
Profile: Ping Scan
```

### Zenmap Ping Scan <br/>
<img width="1351" height="710" alt="ip ping scan results" src="https://github.com/user-attachments/assets/94c58916-bef2-4a7b-9ebc-b67cef6b120e" />

---

# 🖥️ Task 4 – Number of Live Hosts

After completing the Ping Scan, the discovered hosts were 3.

### 📸 Hosts results

<img width="779" height="278" alt="image" src="https://github.com/user-attachments/assets/d9b589c0-7c31-4df5-a3bd-386c793204e0" />

---

# 🌐 Task 5 – IP Addresses of Live Hosts

The Zenmap scan results were reviewed to identify the IP addresses of the live hosts.

### Results

| # | IP Address | Status  |
| - | ---------- | ------- |
| 1 | ` 192.168.8.1`  | 🟢 Live |
| 2 | ` 192.168.8.254`  | 🟢 Live |
| 3 | ` 192.168.8.253`  | 🟢 Live |


# 🆔 Task 6 – MAC Addresses

The MAC addresses associated with the discovered hosts were recorded from the available scan information.

### Results

| # | IP Address | MAC Address         |
| - | ---------- | ------------------- |
| 1 | `192.168.8.1`  | `4C:81:25:1E:D3:48` |
| 2 | `192.168.8.254`  | `72:D0:59:AC:B6:0A` |
| 3 | `192.168.8.253`  | `AC-D5-64-AA-AD-31` |

For the local Windows machine, the MAC address can also be checked using:

```cmd
ipconfig /all
```
### Local MAC address
<img width="1084" height="604" alt="image" src="https://github.com/user-attachments/assets/39030c19-5cda-4554-8671-b9f038d2d8ef" />

---

# 🗺️ Task 7 – Network Topology

Zenmap's **Topology** feature was used to visualise the discovered network.

The topology view provides a graphical representation of the hosts discovered during the scan.

The project instructions require the topology output to be saved in **PDF format** and included in the final report.

### Process

1. Open the **Topology** tab in Zenmap.
2. Enable the legend.
3. Review the topology information.
4. Select **Save Graphic**.
5. Select **PDF**.
6. Save the topology diagram.
 
### Network Topology
<img width="1364" height="711" alt="topology" src="https://github.com/user-attachments/assets/ad74dc32-e892-4494-8014-2c5aef91e49f" />


### 📄 Topology File

The generated PDF is stored in the this repository:
<img width="959" height="377" alt="image" src="https://github.com/user-attachments/assets/9a68d904-f856-4151-9b4e-fe19332f56b9" />

# 📊 Final Scan Results

Here is results summarised below:

| Information        | Result          |
| ------------------ | --------------- |
| Local IPv4 Address | `192.168.8.253`       |
| Subnet Mask        | `255.255.255.0` |
| LAN Subnet         | `192.168.8.0/24`    |
| Default Gateway    | ` 192.168.8.1`       |
| Live Hosts         | `3`             |
| Scan Type          | Ping Scan       |
| Scanning Tool      | Zenmap / Nmap   |
| Topology Generated | Yes             |

---
# 🛠️ Problems Encountered & Solutions
During the practical network scanning lab, I encountered a few challenges while identifying the correct network interface, configuring the scan, and interpreting the results.

## 1. Identifying the Correct Network Subnet
### Problem

When I ran: ipconfig, windows displayed multiple network adapters with different IP addresses. For example: 192.168.56. 1 was shown on one adapter, while the active Wi-Fi connection had:

IPv4 Address: 192.168.8.253
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.8.1
This initially caused confusion about which network should be scanned using Zenmap.

### Solution
I reviewed the adapter information and identified the Wi-Fi adapter as the active LAN connection because it had the default gateway: 192.168.8.1.Using the IP address and subnet mask, I determined that the correct network range was: 192.168.8.0/24. I then used this subnet as the target in Zenmap.

## 2. Understanding the VirtualBox Network Adapter
### Problem
The IP address: 192.168.56.1 was displayed by Windows even though I was connected to the network through Wi-Fi. This created uncertainty about whether 192.168.56.0/24 or 192.168.8.0/24 was the correct network to scan.

### Solution
I compared the network adapter information provided by: ipconfig and identified that: 192.168.56.1 belonged to a separate virtual/network adapter. The active Wi-Fi connection was: 192.168.8.253 with: Default Gateway: 192.168.8.1 This helped me understand the difference between a virtual network interface and the physical LAN connection.

## 3. Creating the Network Topology
### Problem
After completing the network scan, I needed to present the discovered hosts in a visual format instead of only documenting the IP addresses and scan output.

### Solution
I used the Topology feature in Zenmap to generate a graphical representation of the discovered network.
I reviewed the topology, enabled the topology legend where required, and saved the topology diagram as a PDF.
The PDF was included in the GitHub repository as supporting project evidence.

---

# 🧠 What I Learned

Through this project, I learned how network discovery can be performed using Zenmap and Nmap.

Key concepts I practised include:

* Check all network adapters before selecting a subnet.
* Identify the active network interface.
* Use the IP address and subnet mask to determine the correct network range.
* Do not assume that every IP address shown by ipconfig belongs to the physical LAN.
* Understand the difference between physical and virtual network adapters.
* Verify discovered hosts before documenting scan results.
* Use ipconfig /all when additional network information needs to be confirmed.
* Save screenshots, scan output, and topology diagrams as evidence of the practical work.
* Document problems and solutions as part of the troubleshooting process.
  
---

# 🔐 Ethical & Security Considerations

Network scanning can provide information about devices connected to a network and should therefore be performed responsibly.

For this project, scanning should be limited to:

* My own computer.
* My own laboratory network.
* Virtual machines that I control.
* Networks where I have explicit permission to perform security testing.

Unauthorised scanning of networks or systems can violate organisational policies or applicable laws.

---

# 📚 References

* Nmap / Zenmap official download page:
  https://nmap.org/download.html

* Nmap official website:
  https://nmap.org/

* NetworkWalks – Zenmap Network Scanning Practice Lab:
  https://networkwalks.com/zenmap-network-scanning-practice-lab/

---

## 🚀 Conclusion

This project provides practical exposure to **network discovery and scanning**, which are important activities in cybersecurity and ethical hacking.

The lab demonstrates how Zenmap can be used to discover live hosts within a local subnet and present the results in both textual and graphical formats.

**Project completed as part of my cybersecurity practical learning journey.**
