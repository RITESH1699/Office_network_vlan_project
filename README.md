# Office Network with VLANs (Cisco Packet Tracer)

A small office network with 3 VLANs, inter-VLAN routing, DHCP,
ACL-based guest isolation, SSH and port security.

## Topology


![Topology](<img width="881" height="632" alt="OFFICE TOPOLOGY" src="https://github.com/user-attachments/assets/324443fc-4786-40e5-b250-af92922a303d" />
)



## IP Plan
| VLAN | Name  | Network         | Gateway       |
|------|-------|-----------------|---------------|
| 10   | Sales | 192.168.10.0/24 | 192.168.10.1  |
| 20   | IT    | 192.168.20.0/24 | 192.168.20.1  |
| 30   | Guest | 192.168.30.0/24 | 192.168.30.1  |

Server: 192.168.20.10 | SW1 management: 192.168.20.2

## Devices
- 1 Router (2911), 1 Switch (2960), 6 PCs, 1 Server

## What I Configured
- VLANs and 802.1Q trunk between R1 and SW1
- Router-on-a-stick inter-VLAN routing
- DHCP pools on R1
- Extended ACL to block Guest from Sales and IT
- SSH (Telnet disabled), encrypted passwords, login banner
- Port security on access ports, unused ports shut down

## Testing
| Test | Result |
|------|--------|
| Sales to IT ping | Success |
| Guest to Sales/IT ping | Blocked by ACL |
| DHCP on all PCs | Success |
| SSH to R1 from IT-PC1 | Success |

## Screenshots


![VLANs](<img width="655" height="245" alt="show vlan brief" src="https://github.com/user-attachments/assets/de9d0a36-8330-400a-8d35-18d554f0385a" />
)




![Ping success](<img width="485" height="535" alt="SALES-PC-PING TO IT-PC " src="https://github.com/user-attachments/assets/094a297a-2ab8-402d-87c7-549aa6734287" />
)




![Guest blocked](<img width="475" height="382" alt="PING-GUEST-FAIL" src="https://github.com/user-attachments/assets/c2849d6d-35d3-4ce7-8956-166616b00037" />
)




![ACL](<img width="597" height="72" alt="ACL" src="https://github.com/user-attachments/assets/40fe579c-d34d-4213-8574-fd872b36d0b6" />
)




![SSH](<img width="650" height="252" alt="SSH-LOGIN" src="https://github.com/user-attachments/assets/8305ca78-abe3-4126-9c26-299e29d0530e" />
)



## Files
- `Office_Network.pkt` - Packet Tracer project
- 
- `R1-config.txt`[R1-CONFIG.txt](https://github.com/user-attachments/files/34513795/R1-CONFIG.txt)
- 
-  `SW1-config.txt`[SW1.txt](https://github.com/user-attachments/files/34513826/SW1.txt)

- 

## Tools
Cisco Packet Tracer

## What I Learned
VLAN segmentation, inter-VLAN routing, DHCP, ACLs,
secure remote access, and troubleshooting with show commands.
