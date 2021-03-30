# # #WEB STACK IMPLEMENTATION (LEMP STACK)
In this project, i implemented the LEMP stack(Linux, Nginx, Mysql and PHP). Recall, that I implemented the LAMP stack in project, the major difference between the lemp and lamp stack is that apache is being replaced with nginx which is a http proxy application with smaller footprints when compared to apache, which make its capable of handling higher load of http requests. Nginx is therefore faster, even though apache is the most popular and better in terms of functionality. From my research, its possible to run both on the same servers - for eg, nginx can be the reverse proxy while apache runs in the back-end.


# # # # STEP0

I spinned up an ubuntu ec2 on aws cloud, named it , opened up port 80 and 22 for ssh and http traffic.

# # # #STEP1-Installing Nginx

Here i updated the linux machine, and installed nginx as shown in the image below, i also confimred that nginx is up and running.

![ED669586-A718-4E65-9865-E68F53DEDEEE_1_105_c](https://user-images.githubusercontent.com/80499748/113030260-44055000-9142-11eb-9a23-a4ff2d67d71d.jpeg)

# # # #STEP2
Here I installed and secured mysql server, that will store and manage date for my website as shown below.

![01482302-DAD8-4140-A9BF-B3D179382CBB_1_105_c](https://user-images.githubusercontent.com/80499748/113030632-ac543180-9142-11eb-80f6-0d672067879a.jpeg)

# # # #STEP3- Installing my code processor-PHP
After installing my web server and relational db, I installed php which will be responsible for processing my code and generating dynamic content for my web server as shown below.

![854265FE-6AA4-42F6-AE55-84CB4FE99E5D_1_105_c](https://user-images.githubusercontent.com/80499748/113030989-048b3380-9143-11eb-83bc-9e5e69b552e2.jpeg)


 # # #STEP4-Configuring Nginx to use PHP processor
 
 After installing php, I added a new directory structure within /var/www for my projectlemp website as the default directory, then i assigned ownership to the curent system user. I then opened a new config file in Nginx's sites-available using nano editor.I then activated my config file by linking it to the nginx's sites-enabled directory so that nginx will use it when next it reloads. Lastly I disabled nginx default host, and created a new index.html for my projectLEMP web root, at the end nginx was reload, and i got the output  as shown below.
 
 ![7EF0DA07-F32E-4844-B15C-2AB45EDD86F7_1_105_c](https://user-images.githubusercontent.com/80499748/113034890-76657c00-9147-11eb-858f-30a5e27091c7.jpeg)
