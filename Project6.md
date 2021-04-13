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

d. the nest step is to format each of the logical volumes, with ext4 filesystem, 
