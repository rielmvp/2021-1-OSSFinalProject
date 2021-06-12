22000240 Gabriel Manalu
# 2021-1-OSSFinalProject: Complete Web Guide for IT Major in HGU

## DEMO VIDEO:

## What does the Complete Web Guide for IT Major in HGU do?
As its name implies, this project provides a complete guide on what the Information Technology (IT) major is and all about it in HGU, via website. It provides all the basic information on the IT major and how you can take it in HGU. The information is spread into four main pages: __1)__ a blog-like page where you can read about certain articles related to the Information Technology major, __2)__ a page that explains what the Information Technology major is and how it is seen globally, __3)__ a page that introduces and explains the Information Technology major in HGU and its path and courses, and finally __4)__ a credit checker for a certain number of credits taken in the IT major.

## Why is this project useful?
Since there is not much exposure to the information on the IT major in HGU, I believed that my project is very useful to satisfy this purpose. Even among IT major students in Handong, most of them might not be aware of what classes to take or what benefits they can gain by choosing the IT major. Other students might also have only vague information about the IT track, and therefore might not choose this major. Additionally, the implementation of a credit checker can be very helpful to guide current IT students on what classes to take. Overall, I think that this project is very practical and useful not only to IT major students, but also to other interested students.

## How do I get started?
(Detailed guide available in __SETUP_GUIDE.md__)\
Primarily by using a Content Management System (CMS) such as Batflat, you are able to create a similar website step by step. Firstly, it is preferred that you should have an ssh server (such as through Raspberry Pi) available. Then you need to setup nginx (an open-source-software used for web servers) in your ssh server. You also need to install PHP 7.2 and related modules. Then after downloading Batflat's latest release, simply fork this repository and its source codes and files (which will be useful even later) so that you will be able to configure nginx batflat site. To do this, insert the file "batflat" into "/etc/nginx/sites-available" directory. Finally, link this into the sites-enabled directory by running the command "sudo ln -s /etc/nginx/sites-available/batflat /etc/nginx/sites-enabled/" in the root directory and restart nginx. __Then, Batflat is up and running! (even though it looks like a default empty blog)__.

In order to modify your website as I did, you need to first figure out how to use Batflat properly. You can do this extensively reading the documentation at https://batflat.org/. Also, when you logged in as an admin in order to edit your websites, you need to check the Modules tab in order to see all modules that are used in your Batflat. You could also add your own modules or improvise the modules.

![module](/img/module.png "module")

Then, you can edit and modify pages in the Pages tab as follows, made intuitively easy by the Batflat layout. One interesting detail to notice here is the template that you are using. This will be the template/theme that you will use for each page (you can see that for each page I used the template index.html).

![pages](/img/pages.png "pages")

The intricate part of Batflat, then, is modifying the theme (or collection of templates) of each page. This is where you will modify the HTML code to your liking. You will need to choose a theme, set it as active, and then edit it (in my case I chose the BatBlog). You can see that for each theme, there is a list of templates you can modify (whether it's the overall template of the page, or the header, footer, sidebar of the page). Here is where I made most of my adjustments and modifications to get the resulting website that I have now. 

![theme](/img/theme.png "theme")
![theme_edit](/img/theme_edit.png "theme_edit")

Most of what I did was changing the code to match my pictures. I also changed all the default pages and their descriptions to fit my final project (such as adding credit links and updating information on main pages).

![credit](/img/credit.png "credit")
![main](/img/main.png "main")

Finally, you could implement a kind of blog for your website, and you could do this by checking the Blog tab and adding new posts. You could see some example setting for the blog and posts below:

![blog_edit](/img/blog_edit.png "blog_edit")
![blog_check](/img/blog_check.png "blog_check")

On top of that, I also implemented a Credit Checker software feature for my Complete IT Web Guide. I was able to do this by forking a certain software, which is the Grade Tracker, found here at https://github.com/goodtaeeun/OSS_final_project. I used the base and roughly kept the same layout however I modified the code by:
1) Changing it to a credit checker which only checks the credit section for a certain major
2) Having it print out the final WEIGHTED GPA as the average of all individual courses' GPA

### Credit Checker
For my Credit Checker implementation, you could open my creditchecker branch and view it. I was able to use this software feature while simultaneously having Batflat on at the same time by hosting the Credit Checker using Github Pages instead.

## Where can I get more help, if I need it?
You could contact me through email, 22000240@handong.edu in order to inquire more about the project or Batflat.
Also, you could see the original github repository for github which contains batflat at: https://github.com/sruupl/batflat
If you would like to make a contribution and don't know how to, please see detailed information in __CONTRIBUTING.md__.
