# Computer Networks Laboratory Programs

Cisco Packet Tracer simulations for the Computer Networks laboratory. The repository covers fundamental networking concepts including LAN switching and hubs, router interface configuration, dynamic host configuration (DHCP), static and default routing, DNS and Web services, Telnet remote access, dynamic routing protocols (RIP & OSPF), and packet TTL life cycle analysis.

## Student Details

| Field | Details |
| --- | --- |
| Name | Sharan S |
| USN | 1BM24CS264 |
| Section | 5J |

## Lab Programs

| File | Experiment | Purpose and Expected Observation |
| --- | --- | --- |
| [`1BM24CS264-CN-LAB1.pkt`](1BM24CS264-CN-LAB1.pkt) | Communication using a switch and a hub | Tests communication between end devices on a switched LAN and a hub-based LAN using ICMP packets. Devices communicate within their respective LANs; the two LAN groups are separate. |
| [`1BM24CS264-CN-LAB2.pkt`](1BM24CS264-CN-LAB2.pkt) | Router interfaces and connectivity testing | Demonstrates router interface addressing and basic connectivity checks. Ping replies, request timeouts, and unreachable messages help identify whether devices and routes can reach one another. |
| [`1BM24CS264-CN-LAB3.pkt`](1BM24CS264-CN-LAB3.pkt) | DHCP configuration within and outside a LAN | Uses a dedicated DHCP server to assign IP addresses across multiple LANs. Configures a router relay (`ip helper-address`) to forward DHCP requests from remote subnets. Verify dynamic IP assignment and inter-LAN connectivity. |
| [`1BM24CS264-CN-LAB4.pkt`](1BM24CS264-CN-LAB4.pkt) | Static and default routing | Configures static routes on intermediate routers and default routes (`0.0.0.0 0.0.0.0`) on edge routers. Use `show ip route` to inspect routing tables and test end-to-end host communication. |
| [`1BM24CS264-CN-LAB5.pkt`](1BM24CS264-CN-LAB5.pkt) | Web Server and DNS configuration within a LAN | Configures HTTP Web Server and DNS Server within a local network. Adds DNS 'A' records for domain resolution (`www.mysite.com`) and verifies access via Command Prompt ping and the PC web browser. |
| [`1BM24CS264-CN-LAB6.pkt`](1BM24CS264-CN-LAB6.pkt) | Telnet remote access to router | Demonstrates remote router administration from a client PC via Telnet. Configures VTY lines (`line vty 0 4`), authentication passwords, and `enable secret`. Verifies active sessions with `show users` and `show ip interface brief`. |
| [`1BM24CS264-CN-LAB7.pkt`](1BM24CS264-CN-LAB7.pkt) | RIP (Routing Information Protocol) dynamic routing | Configures RIP dynamic distance-vector routing on a 3-router topology. Advertises directly connected classful networks, examines RIP routing updates and routing tables (`show ip route`), and confirms host-to-host ping reachability. |
| [`1BM24CS264-CN-LAB8.pkt`](1BM24CS264-CN-LAB8.pkt) | OSPF (Open Shortest Path First) routing protocol | Configures link-state OSPF routing with wildcard masks in Area 0 across multi-router networks. Verifies neighbor relationships, OSPF routing tables (`show ip route ospf`), protocol information (`show ip protocols`), and end-to-end ping connectivity. |
| *Demonstrated via Lab 7 & 8* | Program 9: Packet TTL (Time to Live) / Lifetime demonstration | Demonstrates TTL decrement behavior across multi-hop routing paths in Packet Tracer Simulation Mode. Packets captured at each router hop exhibit a TTL decrement of 1 per hop (e.g., 255 → 254 → 253 → 252). Performed directly on the multi-router topologies of Lab 7 / Lab 8 without requiring a separate `.pkt` file. |

## How to Run

1. Open the required `.pkt` file in **Cisco Packet Tracer**.
2. Allow network link lights to transition from amber/red to green (link state UP).
3. **Host Connectivity Checks**: Open an end device (PC/Laptop), go to **Desktop → Command Prompt**, and run `ping <destination-ip>`.
4. **Web / DNS Testing (Lab 5)**: Open a PC desktop, open **Web Browser**, and navigate to the configured domain (e.g., `http://www.mysite.com`).
5. **Telnet Testing (Lab 6)**: In the PC Command Prompt, run `telnet 10.0.0.1`, authenticate with the configured password, and run `enable` (with the secret password) to access the router remotely.
6. **Router CLI Inspection**:
   - Routing tables: `show ip route` (or `show ip route ospf` for Lab 8)
   - Protocol details: `show ip protocols`
   - Active Telnet users: `show users`
   - Interface status: `show ip interface brief`
7. **TTL Simulation (Program 9)**: In Lab 7 or Lab 8, switch to **Simulation Mode**, dispatch an ICMP PDU between PC0 and PC1, step through using **Capture/Forward**, and click on the PDU at each hop to view the Inbound/Outbound PDU details confirming the TTL decreases by 1 across every router.

## Learning Outcomes

- Compare communication behavior through Layer 1 (Hub) and Layer 2 (Switch) network devices.
- Configure router interface IP addresses and interpret ICMP diagnostic replies (`Destination host unreachable`, `Request timed out`, `Reply`).
- Deploy centralized DHCP services and configure router DHCP relay agents (`ip helper-address`) across subnets.
- Implement static routes and default static routes (`0.0.0.0 0.0.0.0`).
- Deploy fundamental application layer services (DNS and HTTP) within a private network.
- Secure remote router administration using Telnet, VTY access lines, and encrypted privilege passwords.
- Configure and evaluate dynamic Interior Gateway Protocols: Distance-Vector (RIP) and Link-State (OSPF).
- Analyze packet lifetimes and verify hop-by-hop Time To Live (TTL) decrementation in simulation mode.
