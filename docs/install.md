# Lo que hice para instalar

* add `arm_64bit=1` to /boot/config.txt
* configure hostname con `sudo raspi-config`
* change pi password
* sudo apt install btrfs-progs udisks2-btrfs udisks2-btrfs
* Docker
  - apt install apt-transport-https ca-certificates curl gnupg lsb-release
  - curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor
    -o /usr/share/keyrings/docker-archive-keyring.gpg
  - echo \
  "deb [arch=armhf signed-by=/usr/share/keyrings/docker-archive-keyring.gpg]
https://download.docker.com/linux/debian \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list >
/dev/null
  - apt install docker-ce docker-ce-cli containerd.io


https://di-marco.net/blog/it/2020-04-18-tips-disabling_bluetooth_on_raspberry_pi/

dtoverlay=disable-bt
dtoverlay=disable-wifi

dtoverlay=disable-bt,disable-wifi
dtparam=audio=off

sudo systemctl disable hciuart.service
sudo systemctl disable bluetooth.service
systemctl disable wpa_supplicant.service
systemctl disable  raspberrypi-net-mods

dpkg -l|grep -i bluetooth

sudo apt-get purge bluez -y
sudo apt-get autoremove -y
apt purge bluez bluez-firmware pi-bluetooth


sudo apt install stow tmux

cmdline.txt
brd.rd_nr=4


systemctl set-default multi-user.target


## ZRAM

* systemctl disable dphys-swapfile.service
* sudo apt-get purge dphys-swapfile
* sudo apt-get autoremove -y


## For developtment

sudo apt install git bc bison flex libssl-dev make vim



