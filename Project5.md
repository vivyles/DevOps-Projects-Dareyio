# # # # Client-Server Architecture with MySQL

The goal in this project is to configure a web client and a Database server, create a database and user on the db server and be able to access the database created from the client server.
In production environment, web server and database server are usually placed close to each other on the LAN for security purposes .

# Step1- Setting up the DB server.


a) updated repository , and installed mysql-server, after installation , mysql was enabled.
b) after installing mysql server, I ran the secure mysql installation and then i created a database and user, and gave privileges to the user over the database created.
c)Lastly, I edited the mysql config file, and changed the bind-address from 127.0.0.1 to 0.0.0.0, this will make mysql accessible remotely.

<img width="1530" alt="36E06ACD-E707-4A92-B199-72DC39AE8914" src="https://user-images.githubusercontent.com/80499748/114121714-b34a1500-98a3-11eb-8286-12c8f9d44c09.png">
