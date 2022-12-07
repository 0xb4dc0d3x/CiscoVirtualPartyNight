# CiscoVirtualPartyNight

<div dir="rtl">

[فارسی](./READMEFA.md) [English](./README.md)


## نصب بر روی سیستم عامل
تست شده بر روی اوبونتو ۱۸

دانلود کد بر روی سرور :
```bash
curl -O https://raw.githubusercontent.com/0xb4dc0d3x/CiscoVirtualPartyNight/main/ocserv-install.sh
```

قابلیت اجرا کردن فایل با دستور زیر :
```bash
chmod +x ocserv-install.sh
```

اجرا کد با دستور :
```sh
./ocserv-install.sh
``` 
یا 
```sh
sudo bash ocserv-install.sh
``` 

## نصب بر روی Docker
نصب Docker

ساخت image از پروژه در Docker
```bash
docker build -t ocserv https://github.com/0xb4dc0d3x/CiscoVirtualPartyNight.git
```

اجرای سرور در Docker به صورت یک container
```bash
docker run --name ocserv --privileged -p 443:443 -p 443:443/udp -d ocserv
```

افزودن کاربر
```bash
docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd testUserName
```

عوض کردن پسورد کاربر
```bash
docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd testUserName
```

حذف کاربر
```bash
docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd -d testUserName
```

بستن دسترسی کاربر
```bash
docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd -l testUserName
```

باز کردن دسترسی کاربر
```bash
docker exec -ti ocserv ocpasswd -c /etc/ocserv/ocpasswd -u testUserName
```

لیست کردن تمامی کاربر ها با پسورد به صورت هش شده
```bash
docker exec -ti ocserv cat /etc/ocserv/ocpasswd
```

## قابلیت ها

 نصب آسان

 حذف آسان

 افزودن کاربر

 عوض کردن پسورد کاربر

 لیست کردن تمامی کاربر ها

 حذف کاربر

 بستن دسترسی کاربر

 باز کردن دسترسی کاربر


</div>
