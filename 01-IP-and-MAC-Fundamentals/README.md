# 01-IP-and-MAC-Fundamentals

## Objective
Understand IP and MAC addressing with Switch and Router.

## Topology
- Switch: nw_SW1 (2960)
    - PC1: 10.0.0.1/8, GW 10.0.0.254 -> Fa0/1
    - PC2: 10.0.0.2/8, GW 10.0.0.254 -> Fa0/2

- Router: nw_R1 (2911)
    - Fa0/0: 10.0.0.254/8 -> PC3
    - Fa0/1: 192.168.0.254/24 -> PC4

## Key Concepts
- IP: Logical address (Layer 3)
- MAC: Physical address (Layer 2) - seen via `arp -a`
- Gateway: Router interface to leave LAN

## Test
- PC1 ping PC2: Success (same VLAN via switch)
- PC3 ping Router 10.0.0.254: Success
- Show MAC: `ipconfig /all` and `show mac address-table` on switch

## Files
- IP-MAC-Lab.pkt
- Topology Diagram (screenshot)
