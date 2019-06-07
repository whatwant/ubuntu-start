# ubuntu-start


## Create User

```console
$ sudo adduser
```

## Add sudoer

```console
$ visudo
```

## set locale

```console
$ sudo apt-get install language-pack-ko
$ sudo locale-gen ko_KR.UTF-8
$ sudo dpkg-reconfigure locales
$ sudo update-locale LANG=ko_KR.UTF-8 LC_MESSAGES=POSIX
```

## set date/time

```console
$ sudo timedatectl
$ sudo timedatectl list-timezones | grep Seoul
$ sudo timedatectl set-timezone Asia/Seoul
$ sudo timedatectl
$ date
```

## set nano's tabsize

```console
$ nano ~/.nanorc
```

```
set tabsize 4
set tabstospaces
```


## check 32/64 bit

```console
$ uname -m
```


## Install Docker (16.04)

```console
$ sudo apt-get remove docker docker-engine docker.io containerd runc

$ wget https://download.docker.com/linux/ubuntu/dists/xenial/pool/stable/amd64/containerd.io_1.2.5-1_amd64.deb
$ wget https://download.docker.com/linux/ubuntu/dists/xenial/pool/stable/amd64/docker-ce-cli_18.09.6~3-0~ubuntu-xenial_amd64.deb
$ wget https://download.docker.com/linux/ubuntu/dists/xenial/pool/stable/amd64/docker-ce_18.09.6~3-0~ubuntu-xenial_amd64.deb

$ sudo dpkg --install ./containerd.io_1.2.5-1_amd64.deb
$ sudo dpkg --install ./docker-ce-cli_18.09.6~3-0~ubuntu-xenial_amd64.deb
$ sudo dpkg --install ./docker-ce_18.09.6~3-0~ubuntu-xenial_amd64.deb

$ sudo docker run hello-world
```

## Install Nextcloud

```console
$ sudo mkdir -p /srv/install/nextcloud

$ sudo docker run -d \
-p 80:80 \
-v /srv/install/nextcloud:/var/www/html \
nextcloud

$ sudo nano /srv/install/nextcloud/config/config.php
```

```
  'trusted_domains' =>
  array (
    0 => '104.167.xxx.xxx',
    1 => 'cloud.xxx.com',
  ),
```

