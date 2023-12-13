ssh is used for logging into and executing command on a remote computer. the commands is 
`ssh <host name or ip address>`
we can use with username by the using of @ 

`ssh <user>@<hostname OR IP Address>`
`ssh -l <user> <hostname or IP Address>`

for ssh a vlid requirement is valid username for created on the remote system.

for passwordless authentication we need SSH. first need to create the keypair on the client. the keypair have private key + public key with their own.

private key didnot share with everyone . the second key is public key

for creating the ssh key command `ssh-keygen -t rsa`

when we run this command its ask for passpharase this is optional but it give the extra security on our keys.

public key is stored at `/home/user/.ssh/id_rsa.pub`

private key is stored at `/home/user/.ssh/id_rsa`

for coping the ssh key `ssh-copy-id usr@servername-or-ip`

this will coping the public key on to the remote server under the `/home/user/.ssh/authorized_keys`