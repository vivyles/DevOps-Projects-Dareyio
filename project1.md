# # # WEB STACK IMPLEMENTATION (LAMP STACK) IN AWS

This project shows how LAMP stack,(one of the various web stacks) is implementated. LAMP stands for Linux, Apache, MYsql and PHP. Find below a brief description of how these four components work.

Linux is the operating system, linux is chose because of its open-sourceness and flexibility when compared to other operating systems.It acts as the interface btw the user and the web server. Apache , which is the webserver processes requests from the OS and serves up web assets via http, most websites today, run on apache. Mysql- is the relational database used to store data in a format that can be queried using the sql language, mysql is usually a better choice when dealing with business and complex sites. The last of this stack, PHP is the open source scripting lanuguage that works with apache to help create dynamic web pages. HTML is an alternative in this regard but cant be used to dynamically pull out data from the database. Therefore the lamp stack can handle both satic and dynamic pages.
# # # # step1
downloading and installing apache(refer to the read me file to understand what this is, and how it works), (see screenshot below)
![51F31895-4351-4AC1-AD46-E8A2D6E95B08_1_105_c](https://user-images.githubusercontent.com/80499748/112824457-66fb0b80-903f-11eb-80d3-2382ca7cde7b.jpeg)

# # # #step2
use sudo systemctl status apache2 to verify that apache is indeed running.
