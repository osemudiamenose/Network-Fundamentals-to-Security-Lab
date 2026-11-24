# 03 - Network Topologies

## Lab 1: Star Topology
- File: `Star Topology.pkt`
- One Switch connected to multiple PCs in Star shape.
- All PCs in same network, can ping each other.

## Lab 2: Router + 2 Switches + 2 PCs + 1 Server

### Topology
Router 2911 connects two LANs via two switches.
- Router Gig0/0 -> Left Switch Fa0/3
- Router Gig0/1 -> Right Switch0 Fa0/1
- Left Switch Fa0/1 -> PC1
- Left Switch Fa0/2 -> PC2
- Right Switch0 Fa0/2 -> Server0

### IP Addressing Table

| Device | Interface | IP Address | Subnet Mask | Gateway |
| --- | --- | --- | --- | --- |
| Router R1 | Gig0/0 | 10.0.0.1 | 255.0.0.0 | - |
| Router R1 | Gig0/1 | 20.0.0.1 | 255.0.0.0 | - |
| PC1 | Fa0 | 10.0.0.2 | 255.0.0.0 | 10.0.0.1 |
| PC2 | Fa0 | 10.0.0.3 | 255.0.0.0 | 10.0.0.1 |
| Server0 | Fa0 | 20.0.0.2 | 255.0.0.0 | 20.0.0.1 |

**Note:** Router cannot have same network 10.0.0.0/8 on both interfaces. Left LAN uses 10.0.0.0/8, Right LAN uses 20.0.0.0/8.

### Router Configuration (R1)
