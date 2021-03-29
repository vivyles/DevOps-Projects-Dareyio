# # # WEB STACK IMPLEMENTATION (LAMP STACK) IN AWS

This project shows how LAMP stack,(one of the various web stacks) is implementated. LAMP stands for Linux, Apache, MYsql and PHP. Find below a brief description of how these four components work.

Linux is the operating system, linux is chose because of its open-sourceness and flexibility when compared to other operating systems.It acts as the interface btw the user and the web server. Apache , which is the webserver processes requests from the OS and serves up web assets via http, most websites today, run on apache. Mysql- is the relational database used to store data in a format that can be queried using the sql language, mysql is usually a better choice when dealing with business and complex sites. The last of this stack, PHP is the open source scripting lanuguage that works with apache to help create dynamic web pages. HTML is an alternative in this regard but cant be used to dynamically pull out data from the database. Therefore the lamp stack can handle both satic and dynamic pages.
# # # # step1-apache
downloading and installing apache(refer to the read me file to understand what this is, and how it works), (see screenshot below)
![51F31895-4351-4AC1-AD46-E8A2D6E95B08_1_105_c](https://user-images.githubusercontent.com/80499748/112824457-66fb0b80-903f-11eb-80d3-2382ca7cde7b.jpeg)

# # # #step1b
use sudo systemctl status apache2 to verify that apache is indeed running.
![BB10268F-3E66-4B0A-856D-700DD1480C40_1_105_c](https://user-images.githubusercontent.com/80499748/112824849-e557ad80-903f-11eb-91b4-e4da7a0b2d8b.jpeg)

# # # # #step1c
Before the web server can recieve any traffic, tcp port 80 needs to be opened(http runs on port 80, while https(secured) run on 443), i already added a rule on my vm to allow ssh on port 22 (curl http://127.0.0.1:80, can be used to confirm that apache is indeed running.)
![5CCCF877-5285-4863-83FD-A6A377814481_1_105_c](https://user-images.githubusercontent.com/80499748/112825802-108ecc80-9041-11eb-9f28-d4b774648816.jpeg)

Now, i have successfully configured and installed the first two component of the LAMP stack-linuix, and apache.
# # # #step2-mysql
mysql will help to store and manage date for our web server's use.
![55006D7C-A207-412C-BC8B-4A94257A9020_1_105_c](https://user-images.githubusercontent.com/80499748/112827242-ec33ef80-9042-11eb-9857-31a22f01e6c7.jpeg)
after installing mysql server, i used the mysql_secure_installation to runa security script and remove insecure default settings. i confirmed mysql was working by using sudo mysql as shown below:
![DEA66DB8-D57D-4E6A-8C05-7F9FA57A2D08_1_105_c](https://user-images.githubusercontent.com/80499748/112827545-56e52b00-9043-11eb-972e-079297be19fc.jpeg)
Now, I successfully installed the third component of the LAMP stack; the last is PHP.(code processor)- am installing the php package, php-mysql which is a module that allow php to talk to mysql, and then libapache2-mod-php which enable our web server, apache to handle php files.
# # # #step3-php
![2F26F9D6-13D6-49E3-BCEF-578E3DAF549A_1_105_c](https://user-images.githubusercontent.com/80499748/112827782-a75c8880-9043-11eb-8939-919ceff71e5a.jpeg)

After installing php, i used this command php -v to check the version installed. Now that I have successfully installed the LAMP stack, the following dteps and images shows how i test my setup. Here, I used apache virtual host(running more than one website on a single vm, can be ip-based or name based.)

# # # #step4-creating a v.host for my web server
for this project, I created a directory called projectlamp in the /var/www/html directory, and then I assigned ownership to the current system user.
![F3FDAD64-E039-4454-B470-3A24AC2C0D79_1_105_c](https://user-images.githubusercontent.com/80499748/112829666-497d7000-9046-11eb-875a-b6eb318b9f38.jpeg)



