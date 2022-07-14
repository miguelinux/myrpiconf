# Minecraft

based on:
https://teilgedanken.de/Blog/post/setting-up-a-minecraft-server-using-systemd/
and
https://blog.infoitech.co.uk/linux-systemd-service-unit-minecraft/


useradd --uid 1000 --shell /usr/bin/bash --create-home \
--comment "Minecraft User" --groups cdrom,dip,plugdev,lpadmin,lxd \
--home-dir /home/mc  minecraft \

