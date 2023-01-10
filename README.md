# CiscoVirtualPartyNight

## Script Installation
Tested on ubuntu 16.04, 18.04 and 20.04

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
docker build -t cisco https://github.com/0xb4dc0d3x/CiscoVirtualPartyNight.git
```


------------

<details>
<summary>if command gives you an error go with these steps</summary>


<details>
<summary>Step 1</summary>

```bash
git clone https://github.com/0xb4dc0d3x/CiscoVirtualPartyNight.git
```
  
<details>
<summary>Step 2</summary>
  
```bash
cd CiscoVirtualPartyNight
```  
  
<details>
<summary>Part 3</summary>
  
```bash
docker build -t "cisco:Dockerfile" .
```
  
<details>
<summary>Part 4</summary>
  
```bash
docker run --name cisco --privileged -p 443:443 -p 443:443/udp -d cisco:Dockerfile
```  

<details>
<summary>Part 5</summary>
  
```bash
docker exec -ti cisco ocpasswd -c /etc/ocserv/ocpasswd testUserName
```  
</details>
</details>
</details>
</details>
</details>
</details>

------------


Run docker container
```bash
docker run --name cisco --privileged -p 443:443 -p 443:443/udp -d ocserv
```

Add user
```bash
docker exec -ti cisco ocpasswd -c /etc/ocserv/ocpasswd testUserName
```

Change user password
```bash
docker exec -ti cisco ocpasswd -c /etc/ocserv/ocpasswd testUserName
```

Delete user
```bash
docker exec -ti cisco ocpasswd -c /etc/ocserv/ocpasswd -d testUserName
```

Lock user
```bash
docker exec -ti cisco ocpasswd -c /etc/ocserv/ocpasswd -l testUserName
```

Unlock user
```bash
docker exec -ti cisco ocpasswd -c /etc/ocserv/ocpasswd -u testUserName
```

Show all users and their hashed password
```bash
docker exec -ti cisco cat /etc/ocserv/ocpasswd
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
