## How to Create a Virtual Machine in vSphere

Creating a virtual machine (VM) in VMware vSphere enables you to run multiple operating systems on a single physical server. This comprehensive guide outlines the steps to create a VM in vSphere, from logging in to installing an operating system using an ISO image.

### Prerequisites

1. **Access to vSphere**: Ensure you possess the necessary credentials to access your vSphere environment. If you lack access, you can request it through a ticketing system. (https://support.wicki.sbs/en/customer/create-ticket/)

2. **Assigned Resource Pool**: Identify the specific resource pool where you have permissions to create virtual machines.

3. **Operating System ISO**: Prepare an ISO image of the operating system you intend to install on the VM. If the ISO is larger than 100MB, initiate a ticket for an authorized employee to upload the ISO to your datastore.

### Steps to Create a Virtual Machine

#### Step 1: Log In to vSphere

1. Open a web browser and enter the URL or IP address of your vSphere environment. (https://vsphere.wicki.sbs)
2. Input your login credentials (username and password) to access the system.

#### Step 2: Locate Your Assigned Resource Pool

1. After logging in, you'll be greeted by the vSphere dashboard.
2. On the left-hand panel, find and select "Hosts and Clusters" to expand the tree view.
3. Navigate to the appropriate data center, cluster, or host that houses your designated resource pool.

#### Step 3: Create the Virtual Machine

1. Right-click on the specific resource pool where you wish to create the VM.
2. From the context menu, opt for "New Virtual Machine."
3. This action triggers the appearance of the New Virtual Machine Wizard. Proceed by clicking "Next."

#### Step 4: Configuration

1. **Virtual Machine Configuration**: Choose between a custom VM configuration or a typical setup. For heightened control, select "Custom" and proceed by clicking "Next."

2. **Name and Location**: Assign a name to your virtual machine and pinpoint the location within the resource pool where it will be located. Click "Next."

3. **Select Storage**: Determine the storage location for the VM's files. Click "Next."

4. **Select Compatibility**: Opt for the compatibility level for the VM. In most cases, default compatibility suffices. Click "Next."

5. **Select Guest Operating System**: Choose the guest operating system that matches the one you intend to install. If the precise OS isn't listed, choose the closest match. Click "Next."

6. **Customize Hardware**: Configure the number of CPUs, memory, and other hardware parameters to suit your needs. Click "Next."

7. **Select a Network**: Choose the appropriate network connection for the VM. If unsure, default network settings can be selected. Click "Next."

8. **Connect Virtual Disk**: Choose "Datastore ISO image" and select the previously prepared operating system ISO image. This ISO will facilitate the OS installation on the VM. Click "Next."

#### Step 5: Completing the Wizard

1. Review the summary of your VM's configuration. If satisfied, click "Finish" to initiate VM creation.

#### Step 6: Installation

1. Power on the newly created VM and launch the web console.
2. The VM will boot using the ISO image provided earlier. Follow the on-screen instructions to complete the operating system installation.
