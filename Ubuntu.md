---
title: 服务器好玩的东西
date: 2023-03-21 17:39:46
description: 一些初次玩服务器可能会用到的东西。
tags: [Linux, Ubuntu, Sever]
---
# 前言
由于软件安装教程具有时效性，故只放置官网链接。

# 更新系统时间
```bash
cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
```

# 修改主机名
```bash
vim /etc/hostname
vim /etc/hosts
```

# 修改root密码
```bash
passwd
```

# 修改静态 IP
```bash
nmtui #注意设置DNS
```

# 挂载 NTFS 硬盘
```bash
mount -t ntfs-3g /dev/sda3 /mnt/pssd
```

# 开机自动挂载 NTFS 硬盘
```bash
vim /etc/fstab
/dev/sda3 /mnt ntfs-3g defaults 0 0
```

# 系统监控软件
## [s-tui](https://github.com/amanusk/s-tui)
```bash
apt install python3-pip python3-dev -y
pip3 install s-tui
```

# DDNS
## [ddns-go](https://github.com/jeessy2/ddns-go)

# 私有云
## [Nextcloud](https://nextcloud.com)
## [AList](https://github.com/alist-org/alist)

# 免费 SSL 证书
## [acme.sh](https://github.com/acmesh-official/acme.sh)

# MC 服务器
```
#先下载服务器版安装包 https://mcversions.net/
apt install openjdk-17-jre -y
mkdir /etc/minecraft
cd /etc/minecraft
java -Xms2G -Xmx4G -jar server.jar nogui

vim eula.txt
eula=true

vim /lib/systemd/system/minecraft.service
[Unit]
Description=Minecraft Server
Wants=network.target
After=network.target

[Service]
Type=simple
WorkingDirectory=/etc/minecraft/
ExecStart=/usr/bin/java -Xms2G -Xmx4G -jar /etc/minecraft/server.jar nogui
RestartSec=30
Restart=on-failure
KillMode=process
KillSignal=SIGINT
SuccessExitStatus=130
StandardInput=null

[Install]
WantedBy=default.target

systemctl enable minecraft
systemctl start minecraft
#记得在路由器上转发25565端口
```

# 下载器
## [Aria2](https://github.com/P3TERX/aria2.sh)
### [AriaNg](http://ariang.mayswind.net/zh_Hans/)

# 媒体服务器
## [Plex](https://www.plex.tv/)
## [Jellyfin](https://jellyfin.org/)

# 网页版 SSH
## [Sshwifty](https://github.com/nirui/sshwifty)

# 博客
## [Hexo](https://hexo.io/zh-cn/index.html)
### [NexT](https://theme-next.js.org/)
### [Butterfly](https://butterfly.js.org/)

# 科学上网
## [v2rayA](https://v2raya.org/)