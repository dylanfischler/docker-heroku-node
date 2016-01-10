# docker-heroku-node
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

## Description
This is a scaffolding for a Docker deployable Heroku image. The application itself is your typical Node.js + Express application. It comes with a Grunt build task wired for SASS compilation, Bower dependency injection and JS minification. 

## Installation
`npm install` <br/>
`gem install sass` <br />
`npm install grunt-cli bower -g`

## Setup
#### Define your environment
Add `export NODE_ENV=development` (or production) to your environment. 

#### Set up your database
Database configuration details are defined in your environment as well. Add `export DB_USERNAME=username` and `export DB_PASSWORD=password` to your environment. 

## Building
`grunt`

#### Live Building
`grunt development`

## Deploying to Heroku

```
$ heroku create APP_NAME
$ heroku config:set NODE_ENV=production
$ heroku config:set DB_USERNAME=YOUR_DB_USERNAME
$ heroku config:set DB_PASSWORD=YOUR_DB_PASSWORD 
$ heroku config:set DB_HOST=YOUR_DB_HOST
$ heroku plugins:install heroku-docker
$ heroku docker:init
$ heroku docker:release
$ heroku open
```

## Documentation

For more information about using Node.js on Heroku, see these Dev Center articles:

- [Getting Started with Node.js on Heroku](https://devcenter.heroku.com/articles/getting-started-with-nodejs)
- [Heroku Node.js Support](https://devcenter.heroku.com/articles/nodejs-support)
- [Node.js on Heroku](https://devcenter.heroku.com/categories/nodejs)
- [Best Practices for Node.js Development](https://devcenter.heroku.com/articles/node-best-practices)
- [Build and Deploy with Docker](https://devcenter.heroku.com/articles/docker)
