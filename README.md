# Enterprise Network Design: Accounts & Sales Departments

## Objective
Design a network in Cisco Packet Tracer connecting Accounts and Sales departments with proper IP addressing and routing.

---

## Requirements

### Devices per Department
- 2 PCs
- 1 Printer
- 1 Switch

### Network Configuration
- **Network Address:** 192.168.40.0/25
- **Subnet Mask:** 255.255.255.128
- **Router:** 1 (connects both departments)

---

## IP Addressing

| Department | Network | Gateway | Range |
|------------|---------|---------|-------|
| Accounts | 192.168.40.0/25 | 192.168.40.1 | .1 - .126 |
| Sales | 192.168.40.128/25 | 192.168.40.129 | .129 - .254 |

---

## Device Configuration

### Accounts Department
| Device | IP | Gateway |
|--------|-------|---------|
| PC1 | 192.168.40.2 | 192.168.40.1 |
| PC2 | 192.168.40.3 | 192.168.40.1 |
| Printer1 | 192.168.40.4 | 192.168.40.1 |

### Sales Department
| Device | IP | Gateway |
|--------|-------|---------|
| PC3 | 192.168.40.130 | 192.168.40.129 |
| PC4 | 192.168.40.131 | 192.168.40.129 |
| Printer2 | 192.168.40.132 | 192.168.40.129 |

### Router Configuration
- **FastEthernet 0/0 (Accounts):** 192.168.40.1 / 255.255.255.128
- **FastEthernet 0/1 (Sales):** 192.168.40.129 / 255.255.255.128

---

## Implementation Steps

1. **Add devices:** 1 Router, 2 Switches, 4 PCs, 2 Printers
2. **Cable devices:** Connect PCs/Printers to switches; switches to router
3. **Configure router interfaces:** Set IPs as shown above
4. **Configure all devices:** Set IP addresses, subnet mask (255.255.255.128), and default gateway
5. **Enable router interfaces:** Ensure "no shutdown" is applied

---

## Testing

Run ping commands from any PC to verify connectivity:
- `ping 192.168.40.130` (Accounts to Sales)
- `ping 192.168.40.2` (Sales to Accounts)

**Expected Result:** All pings succeed (0% packet loss)

---

## Topology

<img width="1056" height="466" alt="image" src="https://github.com/user-attachments/assets/1a8a4d8a-2292-4079-8e25-ee3776b405c0" />


