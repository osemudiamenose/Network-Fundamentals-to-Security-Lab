Static-Routing-Lab.pkt
Objective: PC1 (10.0.0.2) ping PC2 (192.168.0.2) via static routes
R1: ip route 192.168.0.0 255.255.255.0 12.12.12.2
R2: ip route 10.0.0.0 255.255.255.0 12.12.12.1
Link: 12.12.12.0/24 between R1-R2
Test: Ping success both ways
File: Static-Routing-Lab.pkt
