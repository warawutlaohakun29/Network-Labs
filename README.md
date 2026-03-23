# Network-Labs

A collection of enterprise-level network simulations and configurations using Cisco Packet Tracer.

## 🚀 Project Overview: Enterprise Network Infrastructure
This lab simulates a robust campus network designed for scalability, redundancy, and security. It features a hierarchical design with a Layer 3 Core Switch managing multiple departmental VLANs.

### 🛠️ Key Technical Implementations:
* [cite_start]**VLAN Segmentation:** Divided network into 4 distinct VLANs (Server, HR, Sales, and Guest) to optimize traffic flow and security[cite: 323].
* [cite_start]**High Availability & Redundancy:** * Configured **EtherChannel (LACP)** to aggregate bandwidth and provide link redundancy[cite: 324].
    * [cite_start]Implemented **Spanning Tree Protocol (STP)** with the Core Switch as the Root Bridge to prevent loops[cite: 324].
* [cite_start]**Routing & Services:** * Established **Inter-VLAN Routing** (SVI) for seamless cross-VLAN communication[cite: 325].
    * [cite_start]Configured **DHCP Relay (ip helper-address)** to centralize IP management from a dedicated server[cite: 325].
* [cite_start]**Network Security:** * Applied **Extended Access Control Lists (ACLs)** to isolate Guest traffic from internal servers while maintaining internet access[cite: 326].
    * [cite_start]Configured **NAT/PAT Overload** on the edge router for secure public internet connectivity[cite: 326].

## 📂 Files in this Repository
* **Network-Labs.pkt:** The main Cisco Packet Tracer simulation file.
* **README.md:** Documentation of the project.

## 🧪 Verification & Test Results

To ensure the network was configured correctly according to the security and connectivity requirements, the following tests were performed from the **Guest VLAN (192.168.40.0/24)**:

### 1. Network Security (Access Control List Verification)
* **Test:** Ping from Guest PC to Internal Server (`192.168.10.100`).
* **Result:** `Destination host unreachable` (from Gateway `192.168.40.1`).
* **Conclusion:** The **Extended ACL** is successfully blocking Guest access to the sensitive Server VLAN, effectively isolating the internal network.
* ![e5d8c3cb-974f-461f-801f-3c252100cdf4](https://github.com/user-attachments/assets/66d1faa8-d839-4944-bb41-c2bc0849c921)

### 2. Internet Connectivity (NAT/PAT Verification)
* **Test:** Ping from Guest PC to Public Internet IP (`200.0.0.2`).
* **Result:** `Reply from 200.0.0.2: bytes=32 time<1ms TTL=126`.
* **Conclusion:** **NAT/PAT Overload** and **Default Routing** are working correctly, allowing private internal hosts to access external resources.

### 3. Automatic IP Assignment (DHCP Relay Verification)
* **Test:** Check IP Configuration on Guest PC.
* **Result:** Successfully received IP `192.168.40.10` via DHCP.
* **Conclusion:** The **DHCP Relay (IP Helper-Address)** on the Layer 3 Switch is correctly forwarding requests to the central DHCP Server across VLAN boundaries.
* ![9a5985de-2a7a-42bd-a678-0f7ab6b27856](https://github.com/user-attachments/assets/723fab13-c93e-4a0d-b0d4-0169c2ee5e41)
