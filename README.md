# Computer Networks Laboratory Programs

Cisco Packet Tracer simulations for the Computer Networks laboratory. The four programs cover LAN communication, router connectivity, dynamic IP addressing, and route configuration.

## Student Details

| Field | Details |
| --- | --- |
| Name | Sharan S |
| USN | 1BM24CS264 |
| Section | 5J |

## Lab Programs

| File | Experiment | Purpose and expected observation |
| --- | --- | --- |
| [`1BM24CS264-CN-LAB1.pkt`](1BM24CS264-CN-LAB1.pkt) | Communication using a switch and a hub | Tests communication between end devices on a switched LAN and a hub-based LAN using ICMP packets. Devices communicate within their respective LANs; the two LAN groups are separate. |
| [`1BM24CS264-CN-LAB2.pkt`](1BM24CS264-CN-LAB2.pkt) | Router interfaces and connectivity testing | Demonstrates router interface addressing and basic connectivity checks. Ping replies, request timeouts, and unreachable messages help identify whether devices and routes can reach one another. |
| [`1BM24CS264-CN-LAB3.pkt`](1BM24CS264-CN-LAB3.pkt) | DHCP and address assignment across networks | Uses a DHCP server to assign addresses to clients on two LANs. A router relay forwards DHCP requests from the remote LAN. Verify the assigned IP settings on the clients and test connectivity between the LANs. |
| [`1BM24CS264-CN-LAB4.pkt`](1BM24CS264-CN-LAB4.pkt) | Static and default routing | Configures static routes on the central router and default routes on the edge routers. Use `show ip route` to inspect routing tables and ping between end devices on the two remote LANs. |

## How to Run

1. Open the required `.pkt` file in Cisco Packet Tracer.
2. Allow the network links to become active.
3. Use **Desktop → Command Prompt** on a PC to run the experiment's ping checks.
4. For Lab 4, open each router's **CLI** and enter `show ip route` to inspect its routing table.

## Learning Outcomes

- Compare communication through a switch and a hub.
- Configure router interfaces and interpret common ping results.
- Configure DHCP pools and DHCP relay for multiple LANs.
- Read routing tables and apply static and default routes.
