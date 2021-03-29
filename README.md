# DevOps-Projects-Dareyio


This project shows how LAMP stack,(one of the various web stacks) is implementated.  LAMP stands for Linux, Apache, MYsql and PHP. Find below a brief description of how these four components work.

Linux is the operating system, linux is chose because of its open-sourceness and flexibility when compared to other operating systems.It acts as the interface btw the user and the web server.  Apache , which is the webserver processes requests from the OS and serves up web assets via http, most websites today, run on apache.
Mysql- is the relational database used to store data in a format that can be queried using the sql language, mysql is usually a better choice when dealing with business and complex sites. The last of this stack, PHP is the open source scripting lanuguage that works with apache to help create dynamic web pages. HTML is an alternative in this regard but cant be used to dynamically pull out data from the database. Therefore the lamp stack can handle both satic and dynamic pages.

In this project, I downloaded ubunutu on amazon cloud, which serves as ourfirst component of the LAMP stack, installed and updated apache(which is my web server) and enaled firewall, lastly I opened up port 80 inorde to allow web traffic in.

Secondly, I installed mysql- which serves as the database that stores and manages data for my web server-apache.
Thridly, I installed php, which is the scritping language in the lamp stack. modules that allow php talk to mysql and apache was installed.
After setting up all the four components of the LAMP stack, I created a virtual host,using a2ensite command and set up a directory called projectlamp, created a new config file using vim. Apache was reloaded after taking these steps.
I then created an index.html file, and added some text using the echo command on linux...inputing my ip add, http://18.190.25.12/, showed me the text from the echo command.




# # # # # #Diffcults Experienced.

1. Coming from san entirely different IT background, it took me 18days to wrap my head around understanding basic linux command.. Most times I tried to run a command with the "sudo" permission and get frustrated until someone points that out for me. I decided to quit severally, but then.. I continued.
2. Using ubuntu 20.4 gave me some issues, sshing in via mac , i think they have a compatibility issues.
