# # # # Client-Server Architecture with MySQL

The goal in this project is to configure a web client and a Database server, create a database and user on the db server and be able to access the database created from the client server.
In production environment, web server and database server are usually placed close to each other on the LAN for security purposes .

# Step1- Setting up the DB server.


a) updated repository , and installed mysql-server, after installation , mysql was enabled.
b) after installing mysql server, I ran the secure mysql installation and then i created a database and user, and gave privileges to the user over the database created.
c)Lastly, I edited the mysql config file, and changed the bind-address from 127.0.0.1 to 0.0.0.0, this will make mysql accessible remotely.
