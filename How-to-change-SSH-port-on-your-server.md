# How to change SSH port on your server

To change the SSH port on Ubuntu, you'll need to modify the SSH daemon configuration file. Here are the steps to do this:

1. **Open the SSH Daemon Configuration File:**
   Open the SSH daemon configuration file (`sshd_config`) in a text editor. You will typically need elevated privileges to edit this file. You can use a command-line text editor like `nano` or `vim`. For example:
   ```bash
   sudo nano /etc/ssh/sshd_config
   ```

2. **Locate the 'Port' Directive:**
   Look for the line that starts with `Port`. This line specifies the port on which the SSH server listens. The default is usually `22`. You can change it to any unused port, for example:
   ```
   Port 2222
   ```

3. **Save and Exit:**
   Save the changes and exit the text editor. For `nano`, you can typically do this by pressing `Ctrl + X`, then `Y` to confirm the changes, and finally `Enter` to exit.

4. **Restart the SSH Service:**
   After modifying the configuration file, you need to restart the SSH service for the changes to take effect. Use the following command:
   ```bash
   sudo service ssh restart
   ```

   Alternatively, you can use the following command on more recent Ubuntu versions:
   ```bash
   sudo systemctl restart ssh
   ```

5. **Verify the Changes:**
   You can verify that SSH is now listening on the new port by running:
   ```bash
   netstat -tuln | grep <new_port>
   ```
   Replace `<new_port>` with the port number you specified in the configuration file.

6. **Update Firewall Rules (if applicable):**
   If you are using a firewall, make sure to update the rules to allow traffic on the new SSH port. For example, using `ufw`:
   ```bash
   sudo ufw allow 2222/tcp
   ```
   Replace `2222` with your new SSH port.

Remember that changing the SSH port can enhance security by making it less predictable, but it's also essential to update your firewall rules and remember the new port when connecting.