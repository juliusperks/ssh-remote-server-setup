# ssh-remote-server-setup

https://roadmap.sh/projects/ssh-remote-server-setup


!) Create 2 SSH keys on your local computer (or the computer you will be using to ssh to the remote computer).
    a) ssh-keygen -t ed25519 -C "primary-key" -f ~/.ssh/server_key_1
    b) ssh-keygen -t ed25519 -C "secondary-key" -f ~/.ssh/server_key_2

2) Verify that the keys have been created.
    a) ls -la ~/.ssh/server_key_*

3) Create your virtual machine on your chosen platform (Digital Ocean, AWS, AZURE, etc.)

4) SSH to your to new virtual machine

5) Confirm or create the file .ssh/authorized_keys

6) Copy your new server SSH public keys to the authorized_keys file

7) Use ctrl+d to disconnect from the server

8) Test the ssh keys
    a) ssh -i ~/.ssh/server_key_1 root@YOUR_SERVER_IP
    b) ssh -i ~/.ssh/server_key_2 root@YOUR_SERVER_IP

