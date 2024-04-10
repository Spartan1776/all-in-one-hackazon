# all-in-one-hackazon

Run a docker container include hackazon, apache, mysql, and nodejs with express server

![Hackazon Logo](https://github.com/rapid7/hackazon/blob/master/web/images/Hackazon.png?raw=true "Hackazon Logo")

## About Hackazon
Hackazon is a vulnerable test application site, that incorporates a realistic e-commerce workflow with full functionality and technology commonly used in today’s mobile and web applications.

This guide will allow you to setup a testing environment, enable you to see problems in action from an attacker’s perspective, and identify the fundamental issues which make such attacks possible.

[Hackazon_User's_Guide.pdf](https://community.rapid7.com/servlet/JiveServlet/downloadBody/3452-102-3-8267/Hackazon_User%27s_Guide.pdf)

## How to use this project 

### Clone this repo 
```shell
git clone https://github.com/Spartan1776/all-in-one-hackazon/
cd all-in-one-hackazon/
```

### Configure Docker
If you haven't already installed docker, you'll need to do so. If you're running Ubuntu or a similar Debian-based distro that uses the Advanced Package Tool (APT, or "apt"), you can convert easyDockerInstall to an executable and run the installation file:
```shell
chmod +700 easyDockerInstall
sudo ./easyDockerInstall
```

If easyDockerInstall fails, try running kaliDockerFix
```shell
chmod +700 kaliDockerFix
sudo ./kaliDockerFix
```

### Build and start
Once Docker is installed, start the docker image:
```shell
chmod +700 startDocker
sudo ./startDocker
```

### Wait for 10 seconds and contact the server :
```shell
firefox http://localhost:80

chromium http://localhost:80
```

### Stopping the container
To stop the container, run
```shell
sudo docker stop hackazon
```

### Removing the container
If you want to remove the container entirely, run
```shell
sudo docker rm hackazon
```

Then begin to configure Hackazon (direct link is http://localhost/install/login for the configuration screen) -- the default installer password (printed on startup) is "password". It's also available at the http://localhost/hackazon-db-pw.txt endpoint. You can change the DB password by editing line 13 of https://github.com/Spartan1776/all-in-one-hackazon/blob/master/scripts/start.sh

## Special Thanks
This project is a direct fork (+ a couple of edits) from cmutzel's all-in-one-hackazon project (https://github.com/cmutzel/all-in-one-hackazon) -- thanks for all of the hard work!
