# Network IP Address Management (IPAM) Summary

## 1. Primary Local Network (LAN)
**Supernet:** `192.168.0.0/22`  
**Total Range:** `192.168.0.0` — `192.168.3.255`  
**Subnet Mask:** `255.255.252.0`

| Range | Purpose | Assignment Type |
| :--- | :--- | :--- |
| `192.168.0.100` - `192.168.0.200` | Cameras | Static |
| `192.168.1.1` - `192.168.1.5` | Routers | Static |
| `192.168.1.10` - `192.168.1.50` | Power, Infrastructure | Static |
| `192.168.1.100` - `192.168.1.199` | User Devices | Dynamic (DHCP) |
| `192.168.1.200` - `192.168.1.255` | Lights, Heaters | Dynamic (DHCP) |
| `192.168.2.1` - `192.168.2.199` | Server Hosts | Static / Reserved |
| `192.168.2.200` - `192.168.2.255` | Server IPMI Ports | Static / Reserved |
| `rest` | Unallocated / Reserved | N/A |

---

## 2. Infrastructure & Specialized Networks

### srvnet (Server Network)
* **Subnet:** `10.1.1.0/24`
* **Range:** `10.1.1.0` — `10.1.1.255`
* **Gateway:** Typically `10.1.1.1`
* **Description:** Dedicated infrastructure network for server management or tiered services.

### vpn net (VPN Pool)
* **Subnet:** `10.10.1.0/24`
* **Range:** `10.10.1.0` — `10.10.1.255`
* **Description:** IP pool assigned to remote clients connecting via VPN.

---

## 3. Quick Reference Table

| Network Name | CIDR / Range | Description |
| :--- | :--- | :--- |
| **User DHCP** | `192.168.1.100-200` | Dynamic IPs for workstations/mobile |
| **Server LAN** | `192.168.2.0/24` | Main local server segment |
| **srvnet** | `10.1.1.0/24` | Isolated server network |
| **vpn net** | `10.10.1.0/24` | Remote access clients |

> **Note:** The `192.168.0.0/22` block currently has significant headroom in the `192.168.0.x` and `192.168.3.x` ranges for future expansion.