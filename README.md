# node 

curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -

sudo apt-get install -y build-essential

sudo apt-get install -y nodejs

sudo apt-get install -y git-core

sudo apt-get install -y imagemagick

sudo apt-get install -y ruby-full

sudo gem install sass

sudo npm install -g n

sudo npm install -g pm2

sudo npm install -g bower

sudo npm install -g pm2-logrotate

sudo apt-get install python -y

sudo git clone https://github.com/teamslogup/sg-core-new www

cd www

sudo git clone https://github.com/teamslogup/analytics-new app

sudo npm install

sudo bower install --allow-root

cd app

sudo npm install

sudo bower install --allow-root

cd ..

sudo npm run build

sudo pm2 set pm2-logrotate:max_size 1G

sudo pm2 set pm2-logrotate:retain all

sudo pm2 set pm2-logrotate:compress true

sudo pm2 set pm2-logrotate:dateFormat default

sudo pm2 set pm2-logrotate:rotateInterval ‘* * 23 * * *’

sudo NODE_ENV=production pm2 start app


# update 

cd www

sudo git pull

sudo npm update

sudo bower install --allow-root

cd app

sudo git pull

sudo npm update

sudo bower install --allow-root

cd ..

sudo npm run build

sudo pm2 start app











# redis

sudo apt-get install -y python-software-properties

sudo apt-get install -y redis-server

sudo service redis-server restart
