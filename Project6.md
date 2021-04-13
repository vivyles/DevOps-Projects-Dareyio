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

