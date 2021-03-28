# OpenSSH Public Key Authentication

## Client

### Generate SSH key pair

```sh
ssh-keygen -t rsa
```

### Store public key on remote server

```sh
ssh-copy-id -i ~/.ssh/id_rsa.pub <$USER>@<$SERVER>
```

## Server

### Edit /etc/ssh/sshd_config:

```sh
PasswordAuthentication no
```

### Restart SSH Service

```sh
service ssh restart
```
