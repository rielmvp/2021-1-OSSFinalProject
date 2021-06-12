## Setting up nginx for your ssh server (specifically Raspberry Pi)

1)On the terminal enter the following commands
$ sudo apt-get update
$ sudo apt-get install nginx 
  – Press y and enter
$ sudo service nginx start

2)Then, on your browser, enter the ip address of your server. It should show a webpage that welcomes you to nginx, showing that it is working properly.
->You can find this out by running "$ ifconfig" in the terminal.

3)Go to /var/www/html 
$ cd /var/www/html

4)Install vim
– $ sudo apt-get install vim
» Press y and enter

5)Create a file “index.html” under /var/www/html
– $ sudo vim index.html

## Necessary PHP setup

1)Install PHP 7.2 and Related Modules by entering this command on the terminal
$ sudo apt install php7.2-fpm php7.2-common php7.2-mbstring php7.2-xmlrpc php7.2-sqlite3 php7.2-soap php7.2-gd php7.2-xml php7.2-cli php7.2-curl php7.2-zip

2) Restart nginx by entering this command on the terminal
$ sudo systemctl restart nginx.service

## Downloading and setting up Batflat

1) Download Batflat's latest release by entering the following commands
$ cd /tmp
$ wget https://github.com/sruupl/batflat/archive/master.zip  $ unzip master.zip
$ sudo mv batflat-master /var/www/html/batflat

2) Run the commands below to set the correct permissions for Batflat to adjust the directory permissions
$ sudo chown -R www-data:www-data /var/www/html/batflat/ 
$ sudo chmod -R 755 /var/www/html/batflat/

3) Configure Nginx Batflat site by adding a certain file batflat into /etc/nginx/sites-available\
->You can do this by runnning "$ sudo vim /etc/nginx/sites-available/batflat" and copying all the information in the batflat file in my repository into the batflat file you are adding into nginx\
->Or you can just copy the batflat file in my repository and move it into /etc/nginx/sites-available\
!However, in line 4 in the part "server_name raspberrypi.local;", change raspberrypi.local into <ip address of your server/Raspberry Pi> if it doesn't work

4) Enable Batflat and restart nginx
$ sudo ln -s /etc/nginx/sites-available/batflat /etc/nginx/sites-enabled/
$ $ sudo systemctl restart nginx.service

5) Open a web browser and go to http://raspberrypi.local/ (or use <ip address of your server/Raspberry Pi> if it doesn't work). It will result in a default Batflat display!

6) To log on as an admin and start editing your website, go to http://raspberrypi.local/admin and log in using ID/PW: admin/admin
