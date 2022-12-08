# CiscoVirtualPartyNight


[فارسی](./READMEFA.md) [English](./README.md)

## Script Installation
Tested on ubuntu 18.04

Download and saving script on your server:
```bash
curl -O https://raw.githubusercontent.com/0xb4dc0d3x/CiscoVirtualPartyNight/main/ocserv-install.sh
```

Making script executable
```bash
chmod +x ocserv-install.sh
```

And then just run it:
```sh
./ocserv-install.sh
``` 
or
```sh
sudo bash ocserv-install.sh
``` 

## Docker Installation
Install Docker
Build docker image
```bash
docker build -t ocserv https://github.com/0xb4dc0d3x/CiscoVirtualPartyNight.git
```

Run docker container
```bash
docker run --name ocserv --privileged -p 443:443 -p 443:443/udp -d ocserv
```

Add user
```bash
docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd testUserName
```

Change user password
```bash
docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd testUserName
```

Delete user
```bash
docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd -d testUserName
```

Lock user
```bash
docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd -l testUserName
```

Unlock user
```bash
docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd -u testUserName
```

Show all users and their hashed password
```bash
docker exec -ti ocserv cat /etc/ocserv/ocpasswd
```

## Features
- Easy install
- Easy uninstall
- Add User
- Change Password
- Show All Users
- Delete User
- Lock User
- Unlock User
