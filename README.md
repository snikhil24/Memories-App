# Memories App
Built with the MERN stack (MongoDB, Express, React and NodeJS).

### Introduction

Memories is simple social media app that allows users to post interesting events. It's built in MERN stack. Server (backend) has been deployed in [Heroku](http://heroku.com/) and the client (frontend) in [Netlify](https://www.netlify.com/). 

![alt tag](https://raw.githubusercontent.com/snikhil24/Memories-App/main/Memories-Screenshot.png)

### Technologies used

##### Client

**Frontend**
1. Axios: for making API request
2. Moment: library working for time and date
3. React-file-base64: convert images 
4. Redux: for managing and centralizing application state
5. Redux-thunk: asynchronous actions
6. Material UI: for User Interface

**Backend**
1. body-parser: for sending POST request
2. cors: enable cross origin request
3. express: framework for routing our application
4. mongoose: create models for our posts (MongoDB)
5. nodemon: monitor for any changes in the source and automatically restart your server

**Database**
1. MongoDB ([MongoDB Atlas](https://www.mongodb.com/atlas))

### Setup
In order to run this project locally, follow the below steps:

* Clone the GitHub repository to your local
```
git clone https://github.com/snikhil24/Memories-App.git
```
* Open the Terminal/Command prompt in your local. Below command must be executed by navigating to both Client and Server folder, this will install all the necessary packages needed for this project.
```
npm install
```
* Database - MongoDB Atlas:
  - Create a free account on MongoDB Atlas which is for Database. Check this [link](https://www.mongodb.com/docs/atlas/tutorial/create-new-cluster/) which will guide you to create Cluster. 
  - Once the Cluster is created. In "Database Deployments" page, 
    click on "Connect" -> click on "Connect your application" -> Copy the "application code". The copied application code will be similar to below, replace     <username> and <password> with your credentials.
    ```
    mongodb+srv://<username>:<password>@cluster0.6xxxxxn.mongodb.net/?retryWrites=true&w=majority
    ```
  - Create an .env file inside "Server" folder, which will be used to define the environment variables.
    ```
    CONNECTION_URL = mongodb+srv://<username>:<password>@cluster0.6xxxxxn.mongodb.net/?retryWrites=true&w=majority
    ```
* In Server folder, .env.example shows an example on how to initialize the environment variables.

### Deployment
**Backend**\
The Server (Backend) has been deployed in Heroku. In order to deploy the backend, follow the below steps:
  * Download and install the [Heroku CLI](https://devcenter.heroku.com/articles/heroku-command-line).
  * Initialize a git repository in a new or existing directory
    ```
    $ cd my-project/
    $ git init
    $ heroku git:remote -a <name>
    ```
  * Commit your code to the repository and deploy it to Heroku using Git.
    ```
    $ git add .
    $ git commit -am "make it better"
    $ git push heroku master
    ```
**Frontend**\
The client (Frontend) has been deployed in Netlify. Follow the below steps:
  * Once the account is created, click on "Add a new site"
  * Navigate to Client folder in terminal, execute the below command:
  ```
    npm run build
  ```
  * The Above command will create a build folder inside the Client folder, this is the build which needs to be uploaded to Netlify which will deploy the frontend.
\
*Backend deployment on Heroku process was referred from Heroku official website.*
