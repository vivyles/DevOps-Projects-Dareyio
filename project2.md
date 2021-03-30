# # #WEB STACK IMPLEMENTATION (LEMP STACK)
In this project, i implemented the LEMP stack(Linux, Nginx, Mysql and PHP). Recall, that I implemented the LAMP stack in project, the major difference between the lemp and lamp stack is that apache is being replaced with nginx which is a http proxy application with smaller footprints when compared to apache, which make its capable of handling higher load of http requests. Nginx is therefore faster, even though apache is the most popular and better in terms of functionality. From my research, its possible to run both on the same servers - for eg, nginx can be the reverse proxy while apache runs in the back-end.


# # # # STEP0

I spinned up an ubuntu ec2 on aws cloud, named it , opened up port 80 and 22 for ssh and http traffic.

# # # #STEP1-Installing Nginx

Here i updated the linux machine, and installed nginx as shown in the image below, i also confimred that nginx is up and running.

![ED669586-A718-4E65-9865-E68F53DEDEEE_1_105_c](https://user-images.githubusercontent.com/80499748/113030260-44055000-9142-11eb-9a23-a4ff2d67d71d.jpeg)


