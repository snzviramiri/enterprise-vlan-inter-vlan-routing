# **Enterprise VLAN & Inter-VLAN Routing Network**

## **Project Overview**

This project demonstrates the design and implementation of a small enterprise network using Cisco Packet Tracer.

The network is segmented into three VLANs to separate user devices, servers, and network management traffic. Inter-VLAN communication is provided using Router-on-a-Stick with IEEE 802.1Q trunking.

## **Network Objectives**

* Implement VLAN-based network segmentation
* Configure an 802.1Q trunk between the switch and router
* Configure Router-on-a-Stick inter-VLAN routing
* Assign IP addressing and default gateways
* Provide connectivity between different VLANs
* Verify VLAN, trunk, routing, and end-to-end connectivity
* Document the network in a professional format

## **VLAN Design**

| **VLAN** | **Purpose** | **Network** | **Default Gateway** |
|---|---|---|---|
| VLAN 10 | Users | 192.168.10.0/24 | 192.168.10.1 |
| VLAN 20 | Servers | 192.168.20.0/24 | 192.168.20.1 |
| VLAN 30 | Management | 192.168.30.0/24 | 192.168.30.1 |

## **Network Architecture**

The network consists of:

* R1 — Router providing inter-VLAN routing
* SW1 — Layer 2 switch providing VLAN segmentation
* VLAN 10 — User network
* VLAN 20 — Server network
* VLAN 30 — Management network
* End devices connected to their respective VLANs

## **Router-on-a-Stick Design**

R1 uses subinterfaces on the physical interface connected to SW1:

* G0/0.10 → VLAN 10 → 192.168.10.1/24
* G0/0.20 → VLAN 20 → 192.168.20.1/24
* G0/0.30 → VLAN 30 → 192.168.30.1/24

The router interface and switch interface are connected using an IEEE 802.1Q trunk.

## **Data Flow**

Traffic between VLANs follows this path:

```text
User PC
   ↓
SW1
   ↓
802.1Q Trunk
   ↓
R1
   ↓
Inter-VLAN Routing
   ↓
Destination VLAN
   ↓
Server / Management Device
```

For example, traffic from a VLAN 10 user accessing a VLAN 20 server is routed through R1 before being delivered to the server.

## **Verification & Testing**

The following commands were used to verify the implementation:

```text
show vlan brief
show interfaces trunk
show ip interface brief
show running-config
```

Connectivity was tested using ICMP:

```text
ping 192.168.20.X
ping 192.168.30.X
```

Successful replies confirmed connectivity between the VLANs.

## **Key Technologies**

* Cisco Packet Tracer
* VLANs
* IEEE 802.1Q
* Trunking
* Router-on-a-Stick
* Inter-VLAN Routing
* IPv4 Addressing
* ICMP
* Network Segmentation
* Cisco IOS CLI

## **Skills Demonstrated**

This project demonstrates practical experience with:

* VLAN configuration
* Switch port configuration
* Trunk configuration
* Router subinterfaces
* Inter-VLAN routing
* IP addressing
* Network troubleshooting
* Connectivity verification
* Network documentation
* Enterprise network design

## **Project Evidence**

Screenshots included in this repository demonstrate:

1. Complete network topology
2. VLAN configuration and verification
3. 802.1Q trunk verification
4. Successful inter-VLAN connectivity testing

## **Lab Environment**

**Platform:** Cisco Packet Tracer

**Network Type:** Small Enterprise Network

**Routing Method:** Router-on-a-Stick

**VLANs:** 10, 20, 30
