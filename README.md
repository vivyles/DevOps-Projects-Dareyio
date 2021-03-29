# DevOps-Projects-Dareyio


This project shows how LAMP stack,(one of the various web stacks) is implementated.  LAMP stands for Linux, Apache, MYsql and PHP. Find below a brief description of how these four components work.

Linux is the operating system, linux is chose because of its open-sourceness and flexibility when compared to other operating systems.It acts as the interface btw the user and the web server.  Apache , which is the webserver processes requests from the OS and serves up web assets via http, most websites today, run on apache.
Mysql- is the relational database used to store data in a format that can be queried using the sql language, mysql is usually a better choice when dealing with business and complex sites. The last of this stack, PHP is the open source scripting lanuguage that works with apache to help create dynamic web pages. HTML is an alternative in this regard but cant be used to dynamically pull out data from the database. Therefore the lamp stack can handle both satic and dynamic pages.

# # # # step1: 
First I spinned up an ubuntu machine on aws cloud,downloaded the private key on my local machine and locked down access using chmod 400(this gives a user read permission only, and remove everything else). after this, I installed apache and updated the firewall as shown below:
