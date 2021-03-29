# # # WEB STACK IMPLEMENTATION (LAMP STACK) IN AWS

This project shows how LAMP stack,(one of the various web stacks) is implementated. LAMP stands for Linux, Apache, MYsql and PHP. Find below a brief description of how these four components work.

Linux is the operating system, linux is chose because of its open-sourceness and flexibility when compared to other operating systems.It acts as the interface btw the user and the web server. Apache , which is the webserver processes requests from the OS and serves up web assets via http, most websites today, run on apache. Mysql- is the relational database used to store data in a format that can be queried using the sql language, mysql is usually a better choice when dealing with business and complex sites. The last of this stack, PHP is the open source scripting lanuguage that works with apache to help create dynamic web pages. HTML is an alternative in this regard but cant be used to dynamically pull out data from the database. Therefore the lamp stack can handle both satic and dynamic pages.
# # # # step1
downloading and installing apache(refer to the read me file to understand what this is, and how it works), (see screenshot below)
![51F31895-4351-4AC1-AD46-E8A2D6E95B08_1_105_c](https://user-images.githubusercontent.com/80499748/112824457-66fb0b80-903f-11eb-80d3-2382ca7cde7b.jpeg)

# # # #step2
use sudo systemctl status apache2 to verify that apache is indeed running.
![BB10268F-3E66-4B0A-856D-700DD1480C40_1_105_c](https://user-images.githubusercontent.com/80499748/112824849-e557ad80-903f-11eb-91b4-e4da7a0b2d8b.jpeg)

# # # # #step3
Before the web server can recieve any traffic, tcp port 80 needs to be opened(http runs on port 80, while https(secured) run on 443), i already added a rule on my vm to allow ssh on port 22 (curl http://127.0.0.1:80, can be used to confirm that apache is indeed running.)
![5CCCF877-5285-4863-83FD-A6A377814481_1_105_c](https://user-images.githubusercontent.com/80499748/112825802-108ecc80-9041-11eb-9f28-d4b774648816.jpeg)

Now, i have successfully configured and installed the first two component of the LAMP stack-linuix, and apache.
# # # #step4-mysql
mysql will help to store and manage date for our web server's use.
![55006D7C-A207-412C-BC8B-4A94257A9020_1_105_c](https://user-images.githubusercontent.com/80499748/112827242-ec33ef80-9042-11eb-9857-31a22f01e6c7.jpeg)

