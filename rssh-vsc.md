# Remote SSH for Visual Studio Code

## Prerequisites
- VPN Access
- A virtual machine with login credentials ("user" and "IP")
- Visual Studio Code with Remote-SSH plugin installed (Follow instructions below to install the plugin)

## Installing Remote-SSH Plugin in Visual Studio Code
1. Open Visual Studio Code.
2. Click on the Extensions icon in the Activity Bar on the side of the window.
3. Search for "Remote - SSH" in the Extensions view.
4. Click the Install button for the "Remote - SSH" extension by Microsoft.
5. Wait for the installation to complete.

## Connecting to the Virtual Machine
1. Open a command prompt (CMD).
2. Generate an SSH key pair if you haven't already:

   ```cmd
   ssh-keygen
    ```

3. Navigate to the SSH directory:

    ```cmd
    cd ~/.ssh
    ```
4. Copy your public key to the virtual machine. Replace "user" and "IP" with your VM's login information:

    ```cmd
    scp id_rsa.pub user@IP:/home/user/.ssh/authorized_keys
    ```

5. Open your SSH configuration and paste the following lines into it and ajust to your needs;
   
   ```ssh config
   Host "friendly name"
   HostName IP
   User user
   IdentityFile ~/.ssh/id_rsa
   ```

## Connecting with Visual Studio Code

  1.  Open Visual Studio Code.
  2.  Click the "Remote Explorer" icon in the Activity Bar on the side of the window.
  3.  Click the gear icon at the top of the "Remote Explorer" panel and select "Connect to Host..."
  4.  Choose the "friendly name" you defined in your SSH configuration.
  5.  Visual Studio Code will connect to your virtual machine via SSH, and you can start working on your remote files.

That's it! You have successfully connected your virtual machine to Visual Studio Code using the Remote-SSH plugin.
