
MEAN Stack Deployment to Ubuntu in AWS.

The MEAN stack is a combination of Mongodb(database), Express(backend), Angular(frontend), and Node.js(java runtime).

In this project, I created a web register application based on the MEAN stack.

# # # step 1.-Installed NodeJs
sudo apt instal -y nodejs

# # # step 2- Install MonogoDB
Here, i installed mongodb, started it and verfied its working, i also installed the node package manager and body-parser.(this helps to process the json files)
Next, I created a dir books, and initialized npm project, then added a file called server.js.


# # # step 3- Install express and set up routes to the server.

a. here i used expresss to pass book information to and from the mongodb database.
b. I installed mongoose which provided a schema based solution to model my app data.
c. Created a dir in the books dir called app, then a file routes.js thus books/apps/routes

# # # step 4- Access Routes with AngularJS
Here , am using angularjs to connect my web page with express.

a. created a folder on books dir, and a file , script inside the public folder, thus books/public.
b. opened up a custome tcp port 3300 on my ec2, and cd .. to Books and started my server: node server.js
The output below was obtained.





