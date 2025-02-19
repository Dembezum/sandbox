# Project 1: 1L PC XCP-NG Pool

## Description

This project involves setting up a small pool of 1-liter mini desktops running
**[XCP-NG](https://xcp-ng.org/)**. The pool will be used for testing and
experimenting with various technologies and tools.

`XCP-NG` is a `type 1 hypervisor` based on the `Xen Project`. It will be used to
host different `virtual machines` (VMs). Users will be delegated access to the
setup, allowing them to manage their own VMs. Each user will have the ability
to create, modify, and delete their VMs as needed.

The primary goal of this project is to create a `flexible and scalable`
environment for testing new software, configurations, and network setups. By
using `XCP-NG`, we can efficiently manage resources and provide isolated
environments for different users and projects.

## Hardware Requirements

The hardware setup for this project includes:

- A way of connecting the setup to the internet (WAN).
- **3 x Mini desktops**: These will serve as the physical hosts for the
`XCP-NG` hypervisor. Each mini desktop will contribute to the pool, providing
CPU, memory, and storage resources for the VMs.
- **1 x Cisco Router**: This router will manage network traffic and provide
connectivity between the mini desktops.
- **1 x Cisco Switch**: The switch will facilitate communication between the
mini desktops and other network components, ensuring efficient data transfer
and network performance.
- **3 x USB -> Ethernet adapters**: These adapters will be used to provide
additional network interfaces for the mini desktops, allowing for better
network management and failover if desired.

## Objectives Network

1. **VLANS**: Create and configure VLANS on the switch to segment the network.
2. **Inter-VLAN Routing**: Configure the router to allow communication between vlans.
3. **DHCP**: Setup a DHCP server to provide IP addresses to devices on the network.
4. **Port Security**: Enable port security on the switch to prevent unauthorized access.

## Objectives Server

1. **Setup and Configuration**: Install and configure `XCP-NG` on the mini
desktops, ensuring they are properly networked and can communicate with each
other.
2. **User Management**: Create user accounts and delegate access to the VMs,
allowing users to manage their own virtual environments.
3. **Testing and Experimentation**: Use the setup to test various technologies,
tools, and configurations, documenting the results and any issues encountered.
4. **Scalability**: Evaluate the scalability of the setup, determining how
additional resources can be added to the pool as needed.
5. **Storage Management**: Configure storage repositories for the VMs.

## Benefits

- **Isolated Testing Environment**: Provides a safe and isolated environment
for testing new software and configurations without impacting production
systems.
- **Resource Management**: Efficiently manages hardware resources, allowing for
the creation of multiple VMs on a single physical host.
- **User Flexibility**: Users have the freedom to manage their own VMs.

## Useful Links

- [XCP-NG Documentation](https://xcp-ng.org/docs/)
- [Xen Project](https://xenproject.org/)
- [Cisco Router Configuration](htps://github.com/dembezum/sandbox/projects/proj1/r1.md)
- [Cisco Switch Configuration](htps://github.com/dembezum/sandbox/projects/proj1/sw1.md)
