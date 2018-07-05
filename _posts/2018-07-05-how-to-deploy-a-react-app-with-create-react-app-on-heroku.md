---
layout: default
title: How to deploy a React app with create-react-app on Heroku
email: joshi.alonzo@gmail.com
category: heroku
---

<div class="alert alert-warning" role="alert">
  Note: Code beginning with $ (dollar sign) implies a terminal command.
</div>

#### 1. Create Heroku Account

#### 2. Install Heroku

Run this from your terminal. The following will add our apt repository and install the CLI:

<kbd>
  $ sudo add-apt-repository "deb https://cli-assets.heroku.com/branches/stable/apt ./"
</kbd>

<kbd>
  $ curl -L https://cli-assets.heroku.com/apt/release.key | sudo apt-key add -
</kbd>

<kbd>
  $ sudo apt-get update
</kbd>

<kbd>
  $ sudo apt-get install heroku
</kbd>

#### 3. Log into Heroku

Enter email and password

<kbd>
  $ heroku login
</kbd>

#### 4. Get into the repository of your app:

<kbd>
  $ cd repository/of/your/app/
</kbd>

#### 5. Create heroku app

Create a heroku app called "webcams-sole-react". We especify a buildpack in order to run react server.

<kbd>
  $ heroku create webcams-sole-react --buildpack https://github.com/mars/create-react-app-buildpack.git
</kbd>

Check out your remotes, you must have a heroku remote

<kbd>
  $ git remote -v
</kbd>

#### 6. Create the Procfile

Create a file with the following content, this is the command to run a server

<kbd>
  web: npm start
</kbd>

#### 7. Run heroku app locally before to production

This app must run on localhost:5000

<kbd>
  $ heroku local web
</kbd>

#### 8. Make a deployment to the web

Make a push

<kbd>
  $ git push heroku master
</kbd>

Ensure that at least one instance of the app is running

<kbd>
  $ heroku ps:scale web=1
</kbd>

Visit the app on web

<kbd>
  $ heroku open
</kbd>

#### References
* [Getting Started on Heroku with Node.js](https://devcenter.heroku.com/articles/getting-started-with-nodejs#introduction)
* [Heroku Buildpack for create-react-app](https://github.com/mars/create-react-app-buildpack)
* [Deploying any React app on Heroku](https://hackernoon.com/deploying-any-react-app-to-heroku-1ee6db9b97d3)
* [Deploying React with Zero Configuration](https://blog.heroku.com/deploying-react-with-zero-configuration)
