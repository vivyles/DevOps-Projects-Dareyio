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

![25062AF3-251C-4EBC-9BC4-8DFA482C9117_1_105_c](https://user-images.githubusercontent.com/80499748/113912748-59a4f600-9790-11eb-9cb3-fe4203580b95.jpeg)


# # # #step2- What my Todo application should  do- three basic http action- post, get and delete.(create new task, display list of all tasks, and then delete a completed task.)
a. I created a routes dir , and created a file called api.js. Since our application is going to fetch data from mongodb, we need to create a model(this is whatmakes it interactive).
b. for the line in a. above to work, i installed mongoose(npm install mongoose).
c. created a folder called models, which contains a file called todo.js.
d. after doing the above steps, i created a cluster on mongodb atlas.
e. in my Todo dir, i created a file named .env, and added the connection string to access my db in it.

N/B: Using environment variables is more secured than adding the connection strings directly to the index.js file., I started my server(node index.js, and got database connected as shown on the imgae below).
At this point,i have my backend configured .

![99FF68B5-5C36-4A33-8341-5C8072198542_1_105_c](https://user-images.githubusercontent.com/80499748/113914438-66c2e480-9792-11eb-9dfa-88cd52276650.jpeg)


# # # #step3- Testing the backend code using Restful API. (here, i used Postman as the API dev client to test my code, as I haven't created the UI yet)

a. after installing and configuring postman, I created a GET and POST request to my API http://3.15.201.71:5000/api/todos as shown below.

![0F20D757-B012-44CA-B5FA-3151B1BD7C88_1_105_c](https://user-images.githubusercontent.com/80499748/113915386-97574e00-9793-11eb-964c-39b7155e676b.jpeg)


