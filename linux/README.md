# Linux commands

## SSH
- Generate a new ssh key
    ```
    ssh-keygen -t rsa -b 4096 -C "m@tthias.space"
    ```
- Add ssh.pub key to remote system, to do password free login
    ```
    ssh-copy-id -f username@remoteHost
    ssh-copy-id -i path/to/key.pub -f username@remoteHost
    ```