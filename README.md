IPTV-APP

## Project Proposal
The plan is to make a web application where users can log in and watch channels. The application will be responsive, so that it can be used on computers or phones.


## Technologies used
* MongoDB - for storing and data manipulating (back-end)
* Express - for framework (back-end)
* AngularJS - structural framework for dynamic web app (front-end)
* Node.js - back-end environment for web apps built with JavaScript


## Prerequisites
* Git 
* Node.js 
* MongoDB
* Bower 
```bash
$ npm install -g bower
```

## Downloading iptv-app 
here are several ways you can get the iptv-app:

### Cloning The GitHub Repository
The recommended way to get iptv-app  is to use git to directly clone the iptv-app repository:

```bash
$ git clone https://github.com/DervisicBerina/iptv-app.git iptv-app
```

This will clone the latest version of the iptv-app repository to a **iptv-app** folder.

### Downloading The Repository Zip File
Another way to use the iptv-app boilerplate is to download a zip copy from the [master branch on GitHub](https://github.com/iptv-app/mean/archive/master.zip). You can also do this using the `wget` command:

```bash
$ wget https://github.com/DervisicBerina/iptv-app.zip -O iptv-app.zip; unzip iptv-app.zip; rm iptv-app.zip
```

Don't forget to rename **mean-master** after your project name.


## Quick Install
Once you've downloaded the boilerplate and installed all the prerequisites, you're just a few steps away from starting to develop your iptv application.

The boilerplate comes pre-bundled with a `package.json` and `bower.json` files that contain the list of modules you need to start your application.

To install the dependencies, run this in the application folder from the command-line:

```bash
$ npm install
```

This command does a few things:
* First it will install the dependencies needed for the application to run.
* If you're running in a development environment, it will then also install development dependencies needed for testing and running your application.
* When the npm packages install process is over, npm will initiate a bower install command to install all the front-end modules needed for the application
* To update these packages later on, just run `npm update`

## Running Your Application

Run your application using npm:

```bash
$ npm start
```

Your application should run on port 3000 with the *development* environment configuration, so in your browser just go to [http://localhost:3000](http://localhost:3000)

That's it! Your application should be running. To proceed with your development, check the other sections in this documentation.
If you encounter any problems, try the Troubleshooting section.

Explore `config/env/development.js` for development environment configuration options.

### Running in Production mode
To run your application with *production* environment configuration:

```bash
$ npm run start:prod
```

Explore `config/env/production.js` for production environment configuration options.

### Running with User Seed
To have default account(s) seeded at runtime:

In Development:
```bash
MONGO_SEED=true npm start
```
It will try to seed the users 'user' and 'admin'. If one of the user already exists, it will display an error message on the console. Just grab the passwords from the console.

In Production:
```bash
MONGO_SEED=true npm start:prod
```
This will seed the admin user one time if the user does not already exist. You have to copy the password from the console and save it.

### Running with TLS (SSL)
Application will start by default with secure configuration (SSL mode) turned on and listen on port 8443.
To run your application in a secure manner you'll need to use OpenSSL and generate a set of self-signed certificates. Unix-based users can use the following command:

```bash
$ npm run generate-ssl-certs
```

Windows users can follow instructions found [here](http://www.websense.com/support/article/kbarticle/How-to-use-OpenSSL-and-Microsoft-Certification-Authority).
After you've generated the key and certificate, place them in the *config/sslcerts* folder.

Finally, execute prod task `npm run start:prod`
* enable/disable SSL mode in production environment change the `secure` option in `config/env/production.js`


## Testing Your Application
You can run the full test suite included with MEAN.JS with the test task:

```bash
$ npm test
```
This will run both the server-side tests (located in the `app/tests/` directory) and the client-side tests (located in the `public/modules/*/tests/`).

To execute only the server tests, run the test:server task:

```bash
$ npm run test:server
```

To execute only the server tests and run again only changed tests, run the test:server:watch task:

```bash
$ npm run test:server:watch
```

And to run only the client tests, run the test:client task:

```bash
$ npm run test:client
```

## Running your application with Gulp

The MEAN.JS project integrates Gulp as build tools and task automation.

We have wrapped Gulp tasks with npm scripts so that regardless of the build tool running the project is transparent to you.

To use Gulp directly, you need to first install it globally:

```bash
$ npm install gulp -g
```

Then start the development environment with:

```bash
$ gulp
```

To run your application with *production* environment configuration, execute gulp as follows:

```bash
$ gulp prod
```

It is also possible to run any Gulp tasks using npm's run command and therefore use locally installed version of gulp, for example: `npm run gulp eslint`


## License
[The MIT License](LICENSE.md)
