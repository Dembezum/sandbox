# Project Network Configuration README.md

## Overview

The network isn't complex as it involves a switch and a router.

## Equipment and Configurations

### Router Configuration (`ttr1`)

- **Hostname**: `ttr1`
- **DHCP Settings**:
  - Excludes specific addresses making sure critical ips are excluded from the scope.
  - Separate DHCP pools for CLIENT and SERVER networks.
  - Specifies default routers, DNS servers, and lease times.
- **Interfaces**:
  - Subinterfaces Configured with IP addresses and NAT settings for WAN and LAN interfaces.
  - VLANs for management (VLAN10), server (VLAN20), (VLAN30) (VLAN40) Virtual, with appropriate addressing.
- **Security**:
  - Access control lists to permit all traffic. (Not safe).
  - SSH, ensuring secure management access.

### Switch Configuration (`ttsw1`)

- **Hostname**: `ttsw1`
- **VLAN Setup**:
  - VLANs for management (VLAN10), server (VLAN20), (VLAN30) (VLAN40) Virtual.
- **Port Security**:
  - Applied on all interface ranges to restrict the network based on MAC addresses.
- **Interface Configurations**:
  - Trunking setup on GigabitEthernet interfaces to allow VLAN traffic.
  - Access port configurations for specific VLANs, supporting various network
  needs, including WAP and server connections.

> Might setup LACP / etherchannel for redundancy and load balancing.

### Access Point Configuration (`ttap1`)

- **Hostname**: `ttap1`
- **DHCP Relay**: Excluded addresses and helper address configured for the client network.
- **Wireless Configuration**:
  - SSID setup with WPA2 security for guest access.
- **Interface**:
  - BVI1 configured with IP addressing and helper address for DHCP relay.

### Server VLAN Details

- Contains 3 XCP-NG hosts configured for high availability and redundancy.

### Client VLAN Details

- Where network dfevices are connected.

## Access vlan Details

- Where end devices are connected.

## Network Services

- **DHCP**: Dynamic Host Configuration Protocol for IP address assignment.
- **NAT**: Network Address Translation for Internet access across the network.
- **VLAN**: Virtual Local Area Networks for segmenting network traffic.
- **SSH**: Secure Shell for encrypted remote management.
- **VPN**: Secure connection to our project.

> DNS to be added.

## Security Features

- **Access Control Lists (ACLs)**: To permit authorized traffic.
- **VPN**: Using our vpn to avoid opening ports and minimize attack surface.
- **Port Security**: To prevent unauthorized access based on MAC addresses.
- **WPA2**: Secure Wi-Fi access.

## Thoughts

This setup is a simple template for networking, but it shouldn't be in any form
of production enviornment.
