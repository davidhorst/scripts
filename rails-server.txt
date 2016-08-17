#!/bin/bash

sudo apt-get update

gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3

curl -L get.rvm.io | bash -s stable

source ~/.rvm/scripts/rvm

rvm requirements

rvmsudo /usr/bin/apt-get install build-essential openssl libreadline6 libreadline6-dev curl git-core zlib1g zlib1g-dev libssl-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt-dev autoconf libc6-dev ncurses-dev automake libtool bison subversion

rvm install 2.2.4

rvm use 2.2.4 --default

rvm rubygems current

gem install rails --no-ri --no-rdoc

gem install passenger

sudo apt-get install libcurl4-openssl-dev

sudo dd if=/dev/zero of=/swap bs=1M count=1024

sudo mkswap /swap

sudo swapon /swap

rvmsudo passenger-install-nginx-module

   install nginx to: /etc/nginx

sudo apt-get install nodejs

sudo apt-get install postgresql postgresql-contrib libpq-dev

sudo su postgres -c psql

CREATE ROLE ubuntu SUPERUSER LOGIN;

sudo apt-get install git

cd /var

sudo mkdir www

cd www

sudo git clone https://github.com/davidhorst/event-viewer.git

sudo chown -R ubuntu event-viewer

sudo touch log/development.log

sudo chmod 0666 /var/www/event-viewer/log/development.log

//change passwords in config/database.yml

rake db:create:all

rake db:migrate

sudo wget https://raw.github.com/JasonGiedymin/nginx-init-ubuntu/master/nginx -O /etc/init.d/nginx

sudo chmod +x /etc/init.d/nginx

cd /etc/init.d

sudo nano nginx

sudo service nginx start

cd /etc/nginx

sudo mkdir sites-available

sudo mkdir sites-enabled

cd conf

sudo vi nginx.conf











