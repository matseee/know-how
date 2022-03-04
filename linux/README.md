# Linux commands
1. [Archive](#Archive)
1. [Cronjobs](#cronjobs)
1. [SSH](#ssh)
1. [Symlinks](#Symlinks)
1. [System monitoring](#system-monitoring)

## Archive
- Create a new compressed archive 
    ```
    // c = create
    // z = compress gzip
    // f = file
    // v = verbose
    tar czfv new.archivew.tgz file.txt folder/
    ```
- Extract archive
    ```
    // x = extract
    tar xzf ostechnix.tgz // in current directory
    tar xzf ostechnix.tgz -C output/path/ // in output path
    ```


## Cronjobs
- Edit current cronjobs
    ```
    sudo contab -e
    ```
- Backup cronjobs
    ```
    sudo crontab -l > /some/shared/location/crontab.bak
    ```
- Import cronjobs
    ```
    sudo crontab /some/shared/location/crontab.bak
    ```
- Crontab job ([generator](https://crontab-generator.org/) / [crontab-guru](https://crontab.guru/))
    ```
    # run script every 5 minutes and output the log into a file.
    */5 * * * * /home/user/script.sh >> /var/log/output.log

    # run script every 5 minutes without log file
    */5 * * * * /home/user/script.sh >/dev/null 2>&1
    ```

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

## Symlinks
- Create a symlink
    ```
    ln -s /path/to/dir_or_file /path/to/new/symlink
    ```

- Remove a symlink
    ```
    rm /path/to/new/symlink
    ```

## System monitoring
- Show disk usage
    ```
    df -h
    ```