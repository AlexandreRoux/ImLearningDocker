FROM debian:latest
MAINTAINER Alexandre 'SuperKoala42' Roux <alexandreroux42@gmail.com>

RUN apt-get update

RUN sudo useradd nagios
RUN sudo groupadd nagcmd
RUN sudo usermod -a -G nagcmd nagios

RUN apt-get install build-essential libgd2-xpm-dev openssl libssl-dev xinetd apache2-utils unzip curl

/* Install Nagios Core */
cd ~
curl -L -O https://assets.nagios.com/downloads/nagioscore/releases/nagios-4.1.1.tar.gz

tar xvf nagios-*.tar.gz

cd nagios-*

./configure --with-nagios-group=nagios --with-command-group=nagcmd --with-mail=/usr/sbin/sendmail

make all

make install

make install-commandmode

make install-init

make install-config

/usr/bin/install -c -m 644 sample-config/httpd.conf /etc/apache2/sites-available/nagios.conf

usermod -G nagcmd www-data

/* Install Nagios Plugins */