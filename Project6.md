# # Web Solution With WordPress

In this project, I worked with a three-tier architecture , learnt disk partitions, and logical volume createion in linux; and demonstrated installing wordpress on one server and connected it remotely to mysql database on a db server.

3 tier-setup;
- PC as client
- -ec2 redhat server as web server(wordpress installed here)
-ec2 redhat as the db server.


#  # # # step 1-Web server preparation;
a. Here I spinned up a web server on aws, and created 3 volumes in the same AZ and attached them to the server.
b. created partition using gdisk, created physical volume using pvcreate command, installed lvm2 and created 2 logical volumes for webdata, and logs out of the pv, and then ut all three in a volume group(like a RAID)
(Note). Logical volume is what the server uses for storage . The idea behind is elasticity; if the lv gets exhausted, a volume can easily be created, added to the vg, and then becomes part of the logical volume, without having to power down the server. sudo vgdisplay -v gave the output below

<img width="1530" alt="07B5963A-B42B-4129-B34D-29802A3E10C8" src="https://user-images.githubusercontent.com/80499748/114501334-a64c5f00-9bde-11eb-8a5e-5991d9bcc882.png">


d. the next step is to format each of the logical volumes, with ext4 filesystem, created /var/www/html for website files and /home/recovery /logs for logs data, and lastly mount each of the lv to the corresponding mount point.
(Note): before mounting the logs lv, its impt to backup the contents of the the logs dir, because when you mount , the original content of the dir gets wiped out,so use the resync utility to backup files in the log dir, and then restore the logs files into the /var/log dir. The last step for the web server config, is to update the /etc/fstab file so that the two mount points will persist after restart. After the daemon was reloaded.

<img width="1530" alt="60579E32-C842-46CA-A0CE-8ADDA75C2029" src="https://user-images.githubusercontent.com/80499748/114501593-2377d400-9bdf-11eb-958a-e559e19dae61.png">




# # # # step 2- preparing the db server.

Just like I did for the web server, I spinned up an ec2 server on aws, created 3 volumes and attached it to the server,then created lv and mounted it to the /db directory(root/dir)

# # # # step3- Db Server Config

1. firstly updated the repository(sum yum update), updated apache and installed php and its dependencies and installed wordpress and copy it to the var/www/html directory.
2. note: Redhat distro comes with certain security policies unlike ubuntu, so we need to set some policies to allow apache work and also allow traffic via http.


# # # # # step 4- Install mysql on the db server 
installed mysql-server and restarted and enabled mysqld.


<img width="1530" alt="3C4BD1D4-BE83-4ABC-966B-9A2BA27423B7" src="https://user-images.githubusercontent.com/80499748/114506748-119a2f00-9be7-11eb-9d87-f697e557278d.png">


# # # # step5-configured DB to work with wordpress

here I created a database, and a user, gave the user complete access to the database, and flushed privileges as shown below:


<img width="1530" alt="D8B29C94-C484-4755-9CFB-E387F3064216" src="https://user-images.githubusercontent.com/80499748/114507402-ec59f080-9be7-11eb-97ce-96e89b4d6350.png">

# # # # step 6- Configured Wordpress to connect to the remote Database.
For the web server to connect to the DB, I installed mysql-client on the web server, then opened tcp port 3306.
Next, I executed this command, sudo mysql -u <db-user> -p -h <DB-Server-Private-IP-address>. Before this can work, I edited the wp-config.php, and changed Db-namme to the name of the DB created, DB-user, anded the specified password.
  
  <img width="1530" alt="96283023-F10D-49B5-AF26-949207A33AC6" src="https://user-images.githubusercontent.com/80499748/114508167-eca6bb80-9be8-11eb-9f87-5fd4642d8de8.png">
  



