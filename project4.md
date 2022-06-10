## MEAN STACK IMPLEMENTATION
### Task
#### In this assignment I'm going to implement a simple Book Register web form using MEAN stack.

## Step 1: I will Install NodeJs
#### Node.js is a JavaScript runtime built on Chrome’s V8 JavaScript engine. Node.js is used in this tutorial to set up the Express routes and AngularJS controllers.

### First I will Update Ubuntu using the code below:

`sudo apt update`

![Update Ubuntu](images/updateubuntu.png)

#### Secondly I will Upgrade ubuntu

![Ubuntu Upgrade](images/upgradeubuntu.png)

#### I added certificates

`sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates`

![Certificate](images/cert1.png)

`curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -`

![Source](images/cert2.png)

### I install NodeJS

`sudo apt install -y nodejs`

![Node](images/node.png)

#### MongoDB stores data in flexible, JSON-like documents. Fields in a database can vary from document to document and data structure can be changed over time.

`sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 0C49F3730359A14518585931BC711F9BA15703C6`

![Key](images/key.png)

`echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.4.list`

![Echo](images/echo.png)

### Install MongoDB

`sudo apt install -y mongodb`

![MongoDB](images/mongo.png)

### Start The server

`sudo service mongodb start`

![Start MongoDB](images/mongo.png)
### Verify that the service is up and running

`sudo systemctl status mongodb`
![Status](images/status.png)

### Install npm – Node package manager.
`sudo apt install -y npm`

![NPM](images/npm.png)

### Install body-parser package

![Body Parser](images/bodyparser.png)

#### We need ‘body-parser’ package to help us process JSON files passed in requests to the server.


#### Create a folder named ‘Books’

`mkdir Books && cd Books`

![Books Directory](images/booksdirectory.png)

#### In the Books directory, Initialize npm project

`npm init`

![NPM Init](images/npminit.png)


#### Add a file to it named server.js

`server.js`

![Server JS](images/catserverjs.png)

## INSTALL EXPRESS AND SET UP ROUTES TO THE SERVER

#### Express is a minimal and flexible Node.js web application framework that provides features for web and mobile applications. We will use Express in to pass book information to and from our MongoDB database.

#### We also will use Mongoose package which provides a straight-forward, schema-based solution to model your application data. We will use Mongoose to establish a schema for the database to store data of our book register.

`sudo npm install express mongoose`

![ExpressandMongoose ](images/expressmongoose.png)

#### In ‘Books’ folder, create a folder named apps

`mkdir apps && cd apps`
![App Directory](images/appdirectory.png)

#### Create a file named routes.js
`vi routes.js`

![Route VI](images/routejs.png)

#### In the ‘apps’ folder, create a folder named models
`mkdir models && cd models`

![Model Directory](images/model.png)
#### Create a file named book.js

`vi book.js`
![VI Book](images/bookjs.png)

## Step 4 – Access the routes with AngularJS

#### AngularJS provides a web framework for creating dynamic views in your web applications. In this tutorial, we use AngularJS to connect our web page with Express and perform actions on our book register. Change the directory back to ‘Books’

#### Create a folder named public

`mkdir public && cd public`
![Public Directory](images/public.png)

#### Add a file named script.js

`vi script.js`

![Script](images/script.png)

#### In public folder, create a file named index.html;
`index.html`

![Index HTML](images/index.png)

#### I Change the directory back up to Books

#### I Start the server by running this command:

`node server.js`

![Node Start](images/success.png)

#### I open Port 3300 in my security group in other to access my webapps on the web, below is the final result

![WEB](images/web.png)
![WEB2](images/web2.png)





