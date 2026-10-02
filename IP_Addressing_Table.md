# IP Addressing Table

## VLAN Networks

| VLAN | Purpose | Network Address | Subnet Mask | Default Gateway |
|---|---|---|---|---|
| VLAN 10 | Users | 192.168.10.0/24 | 255.255.255.0 | 192.168.10.1 |
| VLAN 20 | Servers | 192.168.20.0/24 | 255.255.255.0 | 192.168.20.1 |
| VLAN 30 | Management | 192.168.30.0/24 | 255.255.255.0 | 192.168.30.1 |

## Router Subinterfaces

| Device | Interface | IP Address | Subnet Mask | VLAN | Function |
|---|---|---|---|---|---|
| R1 | G0/0.10 | 192.168.10.1 | 255.255.255.0 | VLAN 10 | Users Gateway |
| R1 | G0/0.20 | 192.168.20.1 | 255.255.255.0 | VLAN 20 | Servers Gateway |
| R1 | G0/0.30 | 192.168.30.1 | 255.255.255.0 | VLAN 30 | Management Gateway |

## End Devices

| Device | VLAN | IP Address | Subnet Mask | Default Gateway |
|---|---|---|---|---|
| User PC(s) | VLAN 10 | 192.168.10.x | 255.255.255.0 | 192.168.10.1 |
| Server(s) | VLAN 20 | 192.168.20.x | 255.255.255.0 | 192.168.20.1 |
| Management Device(s) | VLAN 30 | 192.168.30.x | 255.255.255.0 | 192.168.30.1 |
