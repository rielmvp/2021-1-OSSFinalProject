#Setting up nginx for your ssh server (specifically Raspberry Pi)

1)On the terminal enter the following commands
$ sudo apt-get update
$ sudo apt-get install nginx 
  – Press y and enter
$ sudo service nginx start

2)Then, on your browser, enter the ip address of your server. It should show a webpage that welcomes you to nginx, showing that it is working properly.
->You can find this out by running "$ ifconfig" in the terminal.

3)Go to /var/www/html 
$ cd /var/www/html
Install vim
– $ sudo apt-get install vim
» Press y and enter
Create a file “index.html” under /var/www/html
– $ sudo vim index.html

#Enabling Batflat by using nginx

