# IT351-Project
Project Overview & Objectives
This project focuses on designing, modeling, and simulating a scalable, dual-campus enterprise network topology using Cisco Packet Tracer. The main objective of Phase 1 is to establish the core network infrastructure, connecting two separate geographical sites (Campus A and Campus B) over a WAN serial link. Each campus contains two distinct Local Area Networks (LANs) managed by Cisco 2960 switches, routed through Cisco 2901 routers to ensure structured segment traffic isolation and reliable inter-campus communication.

Network Architecture & Addressing Scheme
LAN Topologies: Four distinct LANs (LAN1 through LAN4) were built across both campuses, connecting multiple end-device PCs to dedicated switches using Copper Straight-Through cables.

IP Addressing Strategy: A structured Class B private IPv4 addressing scheme was adopted using /24 subnets (172.16.10.0/24 to 172.16.40.0/24) for local subnet traffic, paired with default gateway assignments (172.16.x.1) on the router interfaces (GigabitEthernet0/0 and GigabitEthernet0/1).

WAN Link: The point-to-point inter-router connection between Router2 and Router3 was implemented using a dedicated /30 subnet (10.10.10.0/30) over a Serial DCE connection to minimize IP waste and establish a secure WAN link.

Summary of Technical Challenges & Solutions
Throughout the configuration process, several hardware and logical challenges were resolved:

HWIC-2T Hardware Module Installation: Default Cisco 2901 routers lacked built-in serial ports; this was resolved by retrofitting HWIC-2T expansion cards into the router slots.

Subnet Conflict Resolution: Resolved initial IP address overlap errors on router interfaces by systematically flushing stale port configs and reassigning IPv4 gateways sequentially.

WAN Link Activation: Addressed red-status interface link errors by matching precise physical serial interface numbers (e.g., Serial0/2/0) and enabling Port Status: ON across both routers simultaneously.

End-Device Configuration: Standardized static IP configurations and default gateways across all host PCs to ensure seamless local segment routing.

Current Status & Next Steps
Phase 1 Completion Status: 100% Completed. All physical links, switch-to-router interfaces, and inter-router WAN physical connections are fully configured, active, and verified with green link indicators.

