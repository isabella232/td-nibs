---
layout: module
title: Setup
---

## Deploying to Heroku using the Heroku Button

You can deploy your own version of TD-Nibs in seconds using the Heroku button below:

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/treasure-data/td-nibs)
  
## Deploying to Heroku using the Command Line

You can also deploy Nibs to Heroku using the command line:

1. Clone the repository

    ```
    git clone https://github.com/treasure-data/td-nibs
    ```

1. Create a Heroku application

    ```
    cd td-nibs
    heroku create
    ```
    
1. Install the Postgres plugin    

    ```
    heroku addons:add heroku-postgresql:dev
    ```

1. Deploy to Heroku

    ```
    git push heroku master
    ```

1. Run the the application:
    - Open the application in a browser:

        ```
        heroku open
        ```
    - Click the Signup button to create an account
     
    > Facebook login won't work until you complete the Facebook integration steps described below.


## Installing a Local Version 

You can also install Nibs on your local machine:

1. Clone the repository

    ```
    git clone https://github.com/treasure-data/td-nibs
    ```

1. Install the server dependencies

    ```
    cd td-nibs
    npm install
    ```
    
1. Create a local database
    - Install and start [Postgres](http://www.postgresql.org/) on your local machine
    - Create a database called **nibs**
    - If your database is available using **postgres://@127.0.0.1:5432/nibs**, you have nothing else to do
    - If you use another database URL, either define a shell environment variable called **DATABASE_URL**, or modify **server/config.js** to provide your own default URL

1. Start the server    

    ```
    node server
    ```

1. Run the application
    - Open a browser and access the following URL:
        [http://localhost:5000](http://localhost:5000)
    - Click the Signup button to create an account
     

