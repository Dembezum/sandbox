# XCP-NG Pool Setup README

## Overview

This provides basic instructions for setting up a pool of three `XCP-NG`
hosts, with a virtual machine (VM) running Xen Orchestra Appliance (XOA) for
managing the pool. Each user will have their own account with permissions to
create and manage their own virtual machines (VMs).

## Objectives

1. Set up three `XCP-NG` hosts in a pool.
2. Create a VM to host Xen Orchestra Appliance (XOA) for pool management.
3. Configure user accounts and permissions for VM management.

## Prerequisites

- Three mini desktops with `XCP-NG` installed.
- Network infrastructure configured (router and switch).
- `XCP-NG` installation media and access to the internet.

## Steps

### 1. Install `XCP-NG` on Each Host

1. **Prepare Installation Media**:
   - Download the latest `XCP-NG` ISO from the official website.
   - Create a bootable USB drive.

2. **Install `XCP-NG`**:
   - Insert the bootable USB drive into each mini desktop.
   - Boot from the USB drive and follow the on-screen instructions to install `XCP-NG`.
   - Configure the basic settings (hostname, IP address, etc.) during the installation process.

3. **Post-Installation Configuration**:
   - Access each `XCP-NG` host via the console or SSH.
   - Update the system to the latest version using the command perhaps adding the newest repositories:

   ```bash
     yum update -y
     ```

### 2. Create a Pool

1. **Connect to the First Host**:
   - Use `Xen Orchestra` to connect to the first `XCP-NG` host. (Can be created on users pc).

2. **Create a Pool**:
   - In `Xen Orchestra`, create a new pool and add the first host to it.

3. **Add Additional Hosts**:
   - Add the remaining two `XCP-NG` hosts to the pool using the pool management interface.

### 3. Set Up Xen Orchestra Appliance (XOA)

1. **Download XOA**:
   - Download the XOA virtual appliance from the official Xen Orchestra website.

2. **Create a VM for XOA**:
   - In `Xen Orchestra`, create a new VM and upload the XOA virtual appliance.
   - Allocate appropriate resources (CPU, memory, storage) to the XOA VM.

3. **Configure XOA**:
   - Start the XOA VM and follow the on-screen instructions to complete the setup.
   - Access the XOA web interface using the provided IP address.

### 4. User Management

1. **Create User Accounts**:
   - In XOA, navigate to the user management section.
   - Create user accounts for each person who needs access to the pool.

2. **Assign Permissions**:
   - Assign appropriate roles to each user, allowing them to create and manage their own VMs.
   - Ensure that users have permissions to access only their own resources.

### 5. Usage Instructions

1. **Accessing XOA**:
   - Users can access the XOA web interface using the provided IP address and their credentials.

2. **Creating and Managing VMs**:
   - Users can create new VMs by navigating to the VM management section in XOA.
   - Allocate resources (CPU, memory, storage) to each VM as needed.
   - Configure network settings for each VM to ensure connectivity.

3. **Monitoring and Maintenance**:
   - Use XOA to monitor the performance and health of the `XCP-NG` hosts and VMs.
   - Perform regular maintenance tasks such as updates and backups.

## Useful Links

- [XCP-NG Documentation](https://xcp-ng.org/docs/)
