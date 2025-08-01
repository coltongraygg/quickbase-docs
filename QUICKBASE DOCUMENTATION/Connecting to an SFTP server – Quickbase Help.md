## Connecting to an SFTP server

You can connect to folders containing CSV files stored on your SFTP server and sync data into a [connected table](https://helpv2.quickbase.com/hc/en-us/articles/4570308461716-About-Connected-Tables-) in your Quickbase app.

If you haven't connected to an SFTP server before, or you're having trouble connecting, you may want to ask your IT department or your SFTP administrator to help.

To make an SFTP connection, you'll need the following information:

-   **Connection Name**: you can assign any name
-   **Host**: the host name or IP address of the SFTP server. If your host uses a port other than 22, you can also append the port number after the host name/IP address, for example: sftphost.example.com:6022
-   **Username**: your SFTP username
-   **Password**: the password for your SFTP username

Tip

These are the same values that you would use to connect directly to your SFTP server using a client tool such as FileZilla.

## SFTP server information

If you're having trouble connecting, go over the following questions with your IT department or SFTP administrator. Provide Quickbase Tech Support with the answer to these questions if you enter a support case.

**Is port 22 supported? If not, what port should be used for SFTP?**

If your host uses a port other than 22, be sure to append the port number after the host name/IP address when creating the connection, for example: sftphost.example.com:6022

**What are the permissions of the SFTP user making the connection?**

The user must have the read and write permissions necessary to:

-   Create a QuickBase Sync folder in the user's root folder. The exact location will vary depending on how the SFTP server is configured. If the user isn't allowed to create a folder in their root, have the SFTP administrator create the QuickBase Sync folder for them (the name is case sensitive).
-   Create subfolders within the QuickBase Sync folder.
-   Move and rename files within the subfolders of the QuickBase Sync folder.

**Does the SFTP server require public key authentication or some other 2-factor authentication?**

Quickbase currently doesn't support SFTP connections that require public key or some other 2-factor authentication.

**Is the SFTP server behind a firewall that implements IP-filtering?**

Some of the services and features that Quickbase provides, such as connected tables, are hosted in the public cloud. As a result, the list of IP addresses that Quickbase traffic comes from will vary. The list does not change with significant frequency but can change without notice. This means that configuring your firewall to allow the IPs that Quickbase uses may work today, but not tomorrow.

It also means that when the IPs change, the original IPs you configured are no longer under Quickbase control. In other words, someone else’s traffic will come from those IP addresses.

As a result, Quickbase cannot currently recommend nor support configuring your firewall with a list of IP addresses. We recommend that you use the DMZ pattern, which places the SFTP server in an internet-facing zone (wide-open port 22) and has no inbound access to your private network. The private network reaches into the DMZ where the SFTP server resides to read/write data.

**Does the SFTP server use SHA-2?**

New connections can be made only to SFTP servers that use SHA-2. See the list of supported algorithms below.

Supported key algorithms:

-   ecdsa-sha2-nistp256-cert-v01@openssh.com
-   ecdsa-sha2-nistp384-cert-v01@openssh.com
-   ecdsa-sha2-nistp521-cert-v01@openssh.com
-   ssh-ed25519-cert-v01@openssh.com
-   rsa-sha2-512-cert-v01@openssh.com
-   rsa-sha2-256-cert-v01@openssh.com
-   ecdsa-sha2-nistp256
-   ecdsa-sha2-nistp384
-   ecdsa-sha2-nistp521
-   ssh-ed25519
-   sk-ecdsa-sha2-nistp256@openssh.com
-   sk-ssh-ed25519@openssh.com
-   rsa-sha2-512
-   rsa-sha2-256
-   ssh-rsa

Supported kex algorithms:

-   curve25519-sha256
-   curve25519-sha256@libssh.org
-   curve448-sha512
-   ecdh-sha2-nistp521
-   ecdh-sha2-nistp384
-   ecdh-sha2-nistp256
-   diffie-hellman-group-exchange-sha256
-   diffie-hellman-group18-sha512
-   diffie-hellman-group17-sha512
-   diffie-hellman-group16-sha512
-   diffie-hellman-group15-sha512
-   diffie-hellman-group14-sha256
-   ext-info-c

## Limits

Server ID limit = 255 characters