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

1. Download the Nmap/Zenmap package.
2. Run the installation file.
3. Follow the installation wizard.
4. Complete the installation.
5. Open Zenmap.

### 📸 Screenshot

Add your installation screenshot here:

```text
![Zenmap Installation](screenshots/01-zenmap-installation.png)
```

---

# 🌐 Task 2 – Find Local IP Address & LAN Subnet

The Windows Command Prompt was used to identify the local network configuration.

The following command was used:

```cmd
ipconfig
```

This command was used to identify:

* IPv4 Address
* Subnet Mask
* Default Gateway

### Example

```text
IPv4 Address : 10.0.0.X
Subnet Mask  : 255.255.255.0
Gateway      : 10.0.0.1
```

> Replace the example values above with the actual values from your machine.

### 📸 Screenshot

```text
![IP Configuration](screenshots/02-ipconfig.png)
```

---

# 🔎 Task 3 – Discover Live Hosts

Zenmap was used to perform a **Ping Scan** against the local LAN subnet.

The local subnet was entered into Zenmap and the **Ping Scan** profile was selected to identify hosts that were responding on the network.

### Scan Configuration

```text
Target: YOUR-LAN-SUBNET
Profile: Ping Scan
```

For example:

```text
10.0.0.0/24
```

> The subnet above is only an example. I will use the subnet discovered from my own `ipconfig` results.

### 📸 Screenshot

```text
![Zenmap Ping Scan](screenshots/03-ping-scan.png)
```

---

# 🖥️ Task 4 – Number of Live Hosts

After completing the Ping Scan, the discovered hosts were counted.

### Result

```text
Number of live hosts: X
```

> **Note:** The number of hosts will depend on the network being scanned.

### 📸 Screenshot

```text
![Live Hosts](screenshots/04-live-hosts.png)
```

---

# 🌐 Task 5 – IP Addresses of Live Hosts

The Zenmap scan results were reviewed to identify the IP addresses of the live hosts.

### Results

| # | IP Address | Status  |
| - | ---------- | ------- |
| 1 | `X.X.X.X`  | 🟢 Live |
| 2 | `X.X.X.X`  | 🟢 Live |
| 3 | `X.X.X.X`  | 🟢 Live |
| 4 | `X.X.X.X`  | 🟢 Live |

> The addresses above will be replaced with the actual results from my scan.

### 📸 Screenshot

```text
![Live Host IP Addresses](screenshots/05-host-ip-addresses.png)
```

---

# 🆔 Task 6 – MAC Addresses

The MAC addresses associated with the discovered hosts were recorded from the available scan information.

### Results

| # | IP Address | MAC Address         |
| - | ---------- | ------------------- |
| 1 | `X.X.X.X`  | `XX:XX:XX:XX:XX:XX` |
| 2 | `X.X.X.X`  | `XX:XX:XX:XX:XX:XX` |
| 3 | `X.X.X.X`  | `XX:XX:XX:XX:XX:XX` |
| 4 | `X.X.X.X`  | `XX:XX:XX:XX:XX:XX` |

For the local Windows machine, the MAC address can also be checked using:

```cmd
ipconfig /all
```

The project instructions specifically mention using `ipconfig /all` to find the local MAC address.

### 📸 Screenshot

```text
![MAC Addresses](screenshots/06-mac-addresses.png)
```

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

### 📸 Screenshot

```text
![Network Topology](screenshots/07-network-topology.png)
```

### 📄 Topology File

The generated PDF will be stored in the project repository:

```text
results/network-topology.pdf
```

---

# 📊 Final Scan Results

Once the practical scan is completed, the results will be summarised below.

| Information        | Result          |
| ------------------ | --------------- |
| Local IPv4 Address | `X.X.X.X`       |
| Subnet Mask        | `255.255.255.0` |
| LAN Subnet         | `X.X.X.0/24`    |
| Default Gateway    | `X.X.X.X`       |
| Live Hosts         | `X`             |
| Scan Type          | Ping Scan       |
| Scanning Tool      | Zenmap / Nmap   |
| Topology Generated | Yes             |

---

# 📁 Repository Structure

The repository will be organised as follows:

```text
Network-Scanning-with-Zenmap/
│
├── README.md
│
├── screenshots/
│   ├── 01-zenmap-installation.png
│   ├── 02-ipconfig.png
│   ├── 03-ping-scan.png
│   ├── 04-live-hosts.png
│   ├── 05-host-ip-addresses.png
│   ├── 06-mac-addresses.png
│   └── 07-network-topology.png
│
├── results/
│   └── network-topology.pdf
│
└── notes/
    └── lab-notes.md
```

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
