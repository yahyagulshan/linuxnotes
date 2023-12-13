ssh is used for logging into and executing commands on a remote computer. the commands are 

`ssh <host name or IP address>`

we can use with username by using @ 

`ssh <user>@<hostname OR IP Address>`

`ssh -l <user> <hostname or IP Address>`

For SSH, a valid requirement is a valid username created on the remote system.

for passwordless authentication we need SSH. first need to create the keypair on the client. the keypair has a private key + public key with their own.

private key was not shared with everyone. the second key is a public key

for creating the ssh key command `ssh-keygen -t rsa`

when we run this command it asks for a passphrase this is optional but it gives extra security to our keys.

the public key is stored at `/home/user/.ssh/id_rsa.pub`

the private key is stored at `/home/user/.ssh/id_rsa`

for coping the ssh key `ssh-copy-id usr@servername-or-ip`

this will be coping the public key onto the remote server under the `/home/user/.ssh/authorized_keys`
