# sshkey
How to create ssh key

To create an RSA SSH key, just follow this simple command on your local machine:
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

Breakdown:
    -t rsa → generate an RSA key
    -b 4096 → sets the key size to 4096 bits (more secure than 2048)
    -C → adds a label/comment (usually your email)

    Generating public/private rsa key pair.
Enter file in which to save the key (/home/you/.ssh/id_rsa): [Press Enter or specify path]
Enter passphrase (empty for no passphrase): [Type one for security]
Enter same passphrase again: [Repeat it]

If you press Enter, the keys will be saved as:
    ~/.ssh/id_rsa (private key)
    ~/.ssh/id_rsa.pub (public key)

chmod 600 ~/.ssh/id_rsa
chmod 644 ~/.ssh/id_rsa.pub

You can now:
    Add the public key to a Linux server’s ~/.ssh/authorized_keys
    Use it for GitHub, cloud services, or remote login via ssh -i ~/.ssh/id_rsa user@host
