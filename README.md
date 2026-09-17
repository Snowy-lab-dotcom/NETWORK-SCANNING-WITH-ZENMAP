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

* IPv4 Address: 10.0.0.10
* Subnet Mask: 255.255.255.0
* Default Gateway: 10.0.0.1
<br/>
<img width="1277" height="619" alt="image" src="https://github.com/user-attachments/assets/0c572aac-43be-4d49-b63b-6259ac724c54" />

---

# 🔎 Task 3 – Discover Live Hosts

Zenmap was used to perform a **Ping Scan** against the local LAN subnet.

The local subnet was entered into Zenmap and the **Ping Scan** profile was selected to identify hosts that were responding on the network.

### Scan Configuration

```text
Target: 10.0.0.0/24
Profile: Ping Scan
```

### Zenmap Ping Scan <br/>
<img width="1289" height="648" alt="image" src="https://github.com/user-attachments/assets/24baa337-9212-437c-b108-edf95d4b9d4a" />

---

# 🖥️ Task 4 – Number of Live Hosts

After completing the Ping Scan, the discovered hosts were 3.

### 📸 Hosts results

<img width="936" height="299" alt="image" src="https://github.com/user-attachments/assets/7c76402d-a9a0-41b8-9ea4-ca789820072c" />

---

# 🌐 Task 5 – IP Addresses of Live Hosts

The Zenmap scan results were reviewed to identify the IP addresses of the live hosts.

### Results

| # | IP Address | Status  |
| - | ---------- | ------- |
| 1 | `10.0.0.1`  | 🟢 Live |
| 2 | `10.0.0.2`  | 🟢 Live |
| 3 | `10.0.0.10`  | 🟢 Live |


# 🆔 Task 6 – MAC Addresses

The MAC addresses associated with the discovered hosts were recorded from the available scan information.

### Results

| # | IP Address | MAC Address         |
| - | ---------- | ------------------- |
| 1 | `10.0.0.1`  | `52:54:00:12:35:00` |
| 2 | `10.0.0.2`  | `08:00:27:5A:87:BC` |
| 3 | `10.0.0.10`  | `08-00-27-E0-52-44` |

For the local Windows machine, the MAC address can also be checked using:

```cmd
ipconfig /all
```
### Local MAC address
<img width="1229" height="591" alt="image" src="https://github.com/user-attachments/assets/7b2422d0-1c38-4c3b-ad5b-c8adcd407376" />

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
<img width="1308" height="652" alt="image" src="https://github.com/user-attachments/assets/435b0e57-19b3-4500-91cb-cb3ed76b050b" />


### 📄 Topology File

The generated PDF will be stored in the project repository:

<img width="1255" height="636" alt="image" src="https://github.com/user-attachments/assets/96f4c1b4-2402-43cd-a878-87eb42cb4bb4" />


# 📊 Final Scan Results

Here is results summarised below:

| Information        | Result          |
| ------------------ | --------------- |
| Local IPv4 Address | `10.0.0.10`       |
| Subnet Mask        | `255.255.255.0` |
| LAN Subnet         | `10.0.0.0/24`    |
| Default Gateway    | `10.0.0.1`       |
| Live Hosts         | `3`             |
| Scan Type          | Ping Scan       |
| Scanning Tool      | Zenmap / Nmap   |
| Topology Generated | Yes             |

---

# 🧠 What I Learned

Through this project, I learned how network discovery can be performed using Zenmap and Nmap.

Key concepts I practised include:

* Identifying my local IP address.
* Understanding the relationship between an IP address, subnet mask and LAN subnet.
* Performing a Ping Scan to discover live hosts.
* Identifying devices that respond on a local network.
* Reviewing IP and MAC address information.
* Using Zenmap's graphical interface to interpret scan results.
* Creating a visual network topology.
* Documenting cybersecurity practical work using GitHub.
  
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

# 👨🏽‍💻 Project Status

**Status:** 🟡 In Progress

### Progress Checklist

* [ ] Install Zenmap
* [ ] Find local IP address
* [ ] Identify LAN subnet
* [ ] Perform Ping Scan
* [ ] Identify live hosts
* [ ] Record IP addresses
* [ ] Record MAC addresses
* [ ] Generate network topology
* [ ] Save topology as PDF
* [ ] Add screenshots
* [ ] Complete lab questions
* [ ] Finalise GitHub documentation

---

## 🚀 Conclusion

This project provides practical exposure to **network discovery and scanning**, which are important activities in cybersecurity and ethical hacking.

The lab demonstrates how Zenmap can be used to discover live hosts within a local subnet and present the results in both textual and graphical formats.

**Project completed as part of my cybersecurity practical learning journey.**
