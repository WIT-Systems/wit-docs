# WireGuard VPN Setup Guide

Follow these steps to download, install, and configure the WireGuard VPN client, and then import and run a provided tunnel.

## Step 1: Download and Install WireGuard

1. Visit the WireGuard official website to download the WireGuard client for your operating system: [WireGuard Downloads](https://www.wireguard.com/install/).

2. Select the appropriate download link for your OS (e.g., Windows, macOS, Linux) and follow the installation instructions for your platform.

## Step 2: Import a WireGuard Configuration

1. Obtain the WireGuard configuration file (usually ending with `.conf`) that you want to import. This file should be provided to you by your VPN administrator. If you do not have a VPN config for your network, or you have lost it, please go to our [Helpdesk](https://support.wicki.sbs/en/customer/create-ticket/).

2. Open the WireGuard client.

   - **Windows**: Click the WireGuard icon in your system tray and select "Import tunnel(s) from file."
   - **macOS**: Click the WireGuard icon in the menu bar and select "Import Tunnel."
   - **Linux**: Open a terminal and use the `wg-quick` command to import the configuration. For example:

     ```bash
     sudo wg-quick up /path/to/your-config.conf
     ```

3. Navigate to the location where you saved the configuration file and select it.

4. The WireGuard client will import the configuration.

## Step 3: Connect to the VPN Tunnel

1. After importing the configuration, you will see it listed in your WireGuard client.

2. To connect to the VPN tunnel:

   - **Windows**: Click the WireGuard icon in your system tray, locate the imported tunnel, and click "Activate."
   - **macOS**: Click the WireGuard icon in the menu bar, locate the imported tunnel, and click "Activate."
   - **Linux**: Use the following command to activate the tunnel:

     ```bash
     sudo wg-quick up your-config-name
     ```

3. The WireGuard client will establish a connection to the VPN server using the imported configuration.

## Step 4: Verify the Connection

1. To ensure that your connection is active, check the WireGuard client for a green indicator or status that shows you are connected.

2. You can also try to ping the gateway of your private network. It usually consists of  10.2.X.1 with X being the id of your private network.

Congratulations! You have successfully downloaded, installed, imported, and connected to a WireGuard VPN tunnel.
