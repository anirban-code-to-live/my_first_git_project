### Steps to follow for passwordless login using ssh

1. **Create key**  ``ssh-keygen -t rsa``
2. **Copy key to server** ``ssh-copy-id user@server``

If the command *ssh-copy-id* is not available, then ``cat ~/.ssh/id_rsa.pub | ssh remote_username@server_ip_address "mkdir -p ~/.ssh && chmod 700 ~/.ssh && cat >> ~/.ssh/authorized_keys && chmod 600 ~/.ssh/authorized_keys"``

3. **Login to server** ``ssh user@server``


### Bitbucket - SSH Key set up for passwordless git operations

1. **Set up default identity** ``ssh-keygen``
2. **Add the key to the agent** ``ssh-add ~/.ssh/<private_key_file>``
3. **Copy the public key** ``cat /home/anirban/.ssh/<ssh-key-filename>.pub``
4. **Add the public key to bitbucket account** Save the key into manage key section
5. **Test for successful set up** ``ssh -T git@bitbucket.org``

More details here - https://support.atlassian.com/bitbucket-cloud/docs/set-up-an-ssh-key/#SetupanSSHkey-ssh2
