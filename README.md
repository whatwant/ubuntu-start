# ubuntu-start

Create User

adduser


Add sudoer

visudo



check 32/64 bit
uname -m




Install Docker (16.04)

sudo apt-get remove docker docker-engine docker.io containerd runc

wget https://download.docker.com/linux/ubuntu/dists/xenial/pool/stable/amd64/containerd.io_1.2.5-1_amd64.deb
wget https://download.docker.com/linux/ubuntu/dists/xenial/pool/stable/amd64/docker-ce-cli_18.09.6~3-0~ubuntu-xenial_amd64.deb
wget https://download.docker.com/linux/ubuntu/dists/xenial/pool/stable/amd64/docker-ce_18.09.6~3-0~ubuntu-xenial_amd64.deb

sudo dpkg --install ./containerd.io_1.2.5-1_amd64.deb
sudo dpkg --install ./docker-ce-cli_18.09.6~3-0~ubuntu-xenial_amd64.deb
sudo dpkg --install ./docker-ce_18.09.6~3-0~ubuntu-xenial_amd64.deb

sudo docker run hello-world





Install Nextcloud


sudo mkdir -p /srv/install/nextcloud

sudo docker run -d \
-p 80:80
-v /srv/install/nextcloud:/var/www/html \
nextcloud


sudo nano /srv/install/nextcloud/config/config.php

  'trusted_domains' =>
  array (
    0 => '104.167.xxx.xxx',
    1 => 'cloud.xxx.com',
  ),




