# на гостевой машине

sudo apt update
sudo apt install -y ssh
sudo systemctl enable --now ssh
ip a

# на хост машине

ssh-keygen -t ed25519
ssh-copy-id kali@172.20.10.8
ssh kali@172.20.10.8

# создать пользователя с домашней директорией

sudo useradd -m user1
sudo passwd user1
sudo vim /etc/sudoers
sudo vim /etc/pam.d/common-password

# install java

sudo apt install -y openjdk-17-jre


# antivirus

sudo apt install -y clamav cronie
sudo systemctl enable --now cronie
