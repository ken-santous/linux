Installing Docker on Linux

$ sudo apt install docker.io

add our normal user to the docker group

$ sudo usermod -a -G docker $USER

Installing Docker on Windows and OS X

Pulling down the Kali Docker image

$ docker pull kalilinux/kali-linux-docker

running “docker image ls” we can see the image

$ docker image ls

create a folder in our home folder called “Pentest”

$ mkdir ~/Pentest

Think of it like this: “-v <host direcoty>:<container directory>”.
  
$ docker run -v ~/Pentest:/Pentest -t -i kalilinux/kali-linux-docker /bin/bash

Install Kali tools

# apt update
# apt install metasploit-framework
# msfconsole

References
https://docs.docker.com/install/linux/linux-postinstall/

https://www.kali.org/news/official-kali-linux-docker-images/

