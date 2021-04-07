# # Simple To-Do application on MERN Web Stack

# # # In this project, I implemented a web solution based on MERN stack in AWS Cloud.

Note that the mERN stack consists of four components- Mongodb(database), ExpressJS(server side web app), ReactJS(frontend for UI), and Node.js(java runtime enviro).

A user interacts with the reactJS as the frontend, this frontend is served by the application backend throught the expressJS that runs on top of node.js. As the user inputs data via reactJS, the input/output operation is sent throught the node.js based express server, which in turn gets the data from mongodb, data is returned to the frontend application, which the user views.

# # # #step1. 
I have prepped  and updated my ubuntu server on aws cloud, now am going to configure the backend by i
a. nstall node.js on my server
b. mkdir called Todo
c.input command npm init(to initalize my rpoject, which in turn created a file named package.json that contains informtion about my app and all it needs to run well.)
d. next, i installed expressJS,(npm install expressJS), and created index.js file.
Next, i installed dotenv module, with this done correctly, i was able to see my server running on tcp port 5000 (this port was already opened on my ec2)as shown below.


![070E389B-7B65-4DA2-9047-A37CD62AE37A_1_105_c](https://user-images.githubusercontent.com/80499748/113912757-5c9fe680-9790-11eb-8012-bc428826d8a7.jpeg)



