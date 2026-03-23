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

## 📸 Network Topology
*(แนะนำให้น้องบีอัปโหลดรูปภาพ Topology แล้วมาแปะลิงก์ตรงนี้ เพื่อให้คนเห็นภาพรวมทันทีครับ)*
