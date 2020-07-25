### Steps to follow for passwordless login using ssh

1. **Create key**  ``ssh-keygen -t rsa``
2. **Copy key to server** ``ssh-copy-id user@server``

If the command *ssh-copy-id* is not available, then ``cat ~/.ssh/id_rsa.pub | ssh remote_username@server_ip_address "mkdir -p ~/.ssh && chmod 700 ~/.ssh && cat >> ~/.ssh/authorized_keys && chmod 600 ~/.ssh/authorized_keys"``

3. **Login to server** ``ssh user@server``


### SSH Key set up for passwordless git operations

Follow this link - https://support.atlassian.com/bitbucket-cloud/docs/set-up-an-ssh-key/#SetupanSSHkey-ssh2
