22000240 Gabriel Manalu
# 2021-1-OSSFinalProject: Complete Web Guide for IT Major in HGU

## What does the Complete Web Guide for IT Major in HGU do?
As its name implies, this project provides a complete guide on what the Information Technology (IT) major is and all about it in HGU, via website. It provides all the basic information on the IT major and how you can take it in HGU. The information is spread into four main pages: __1)__ a blog-like page where you can read about certain articles related to the Information Technology major, __2)__ a page that explains what the Information Technology major is and how it is seen globally, __3)__ a page that introduces and explains the Information Technology major in HGU and its path and courses, and finally __4)__ a credit checker for a certain number of credits taken in the IT major.

## Why is this project useful?
Since there is not much exposure to the information on the IT major in HGU, I believed that my project is very useful to satisfy this purpose. Even among IT major students in Handong, most of them might not be aware of what classes to take or what benefits they can gain by choosing the IT major. Other students might also have only vague information about the IT track, and therefore might not choose this major. Additionally, the implementation of a credit checker can be very helpful to guide current IT students on what classes to take. Overall, I think that this project is very practical and useful not only to IT major students, but also to other interested students.

## How do I get started?
(Detailed guide available in __SETUP_GUIDE.md__)\
Primarily by using a Content Management System (CMS) such as Batflat, you are able to create a similar website step by step. Firstly, it is preferred that you should have an ssh server (such as through Raspberry Pi) available. Then you need to setup nginx (an open-source-software used for web servers) in your ssh server. You also need to install PHP 7.2 and related modules. Then after downloading Batflat's latest release, simply fork this repository and its source codes and files (which will be useful even later) so that you will be able to configure nginx batflat site. To do this, insert the file "batflat" into "/etc/nginx/sites-available" directory. Finally, link this into the sites-enabled directory by running the command "sudo ln -s /etc/nginx/sites-available/batflat /etc/nginx/sites-enabled/" in the root directory and restart nginx. __Then, Batflat is up and running! (even though it looks like a default empty blog)__



## Where can I get more help, if I need it?
You could contact me through email, 22000240@handong.edu in order to inquire more about the project or Batflat.
Also, you could see the original github repository for github which contains batflat at: https://github.com/sruupl/batflat
If you would like to make a contribution and don't know how to, please see detailed information in __CONTRIBUTING.md__.
