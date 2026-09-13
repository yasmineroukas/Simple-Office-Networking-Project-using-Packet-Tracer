# Cisco Packet Tracer Network Design: Inter-Department Connectivity

This project demonstrates the design, configuration, and verification of a corporate network topology using **Cisco Packet Tracer**. The goal is to connect two distinct organizational units—the **Accounts** and **Delivery** departments—ensuring proper IP addressing, subnetting, cabling, and full end-to-end connectivity test verification.

---

##  Objectives & Requirements

- **Department Topology**: Implement at least 2 end-user PCs per department (**Accounts** and **Delivery**).
- **Infrastructure**: Integrate switches and routers to facilitate local segment switching and inter-network routing.
- **Addressing Scheme**: Utilize the network subnet `192.168.40.0` to assign appropriate IP addresses, subnet masks, and default gateways to all device interfaces.
- **Physical Cabling**: Connect devices using standard Ethernet media (straight-through, crossover, or serial links as required).
- **Verification**: Conduct ping tests from the **Delivery** department PCs to the **Accounts** department PCs to verify full reachability.

---

##  Network Topology & IP Addressing Plan

| Department | Device Name | Interface | IP Address | Subnet Mask | Default Gateway |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Accounts** | PC-Accounts-1 | FastEthernet0 | `192.168.40.2` | `255.255.255.128` | `192.168.40.1` |
| **Accounts** | PC-Accounts-2 | FastEthernet0 | `192.168.40.3` | `255.255.255.128` | `192.168.40.1` |
| **Accounts** | Printer-Accounts-2 | FastEthernet0 | `192.168.40.4` | `255.255.255.128` | `192.168.40.1` |
| **Delivery** | PC-Delivery-1 | FastEthernet0 | `192.168.40.130` | `255.255.255.128` | `192.168.40.129` |
| **Delivery** | PC-Delivery-2 | FastEthernet0 | `192.168.40.131` | `255.255.255.128` | `192.168.40.129` |
| **Delivery** | Printer-Delivery-2 | FastEthernet0 | `192.168.40.132` | `255.255.255.128` | `192.168.40.129` |
---

##  How to Run / Test

1. **Download the File**: Clone or download the `.pkt` (Packet Tracer file) from this repository.
2. **Open in Cisco Packet Tracer**: Launch the topology file in Cisco Packet Tracer (v8.0 or higher recommended).
3. **Verify Configuration**:
   - Inspect individual PC IP configurations via Command Prompt:
     ```cmd
     ipconfig /all
     ```
4. **Test Connectivity**:
   - Open Command Prompt on a **Delivery** PC and ping an **Accounts** PC:
     ```cmd
     ping 192.168.40.2
     ```
   - Ensure `0% loss` to confirm full routing between segments.
