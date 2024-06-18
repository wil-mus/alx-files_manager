0x04. Files manager
===================

`Back-end` `JavaScript` `ES6` `NoSQL` `MongoDB` `Redis` `NodeJS` `ExpressJS` `Kue`


This project is a summary of this back-end trimester: authentication, NodeJS, MongoDB, Redis, pagination and background processing.

The objective is to build a simple platform to upload and view files:

-   User authentication via a token
-   List all files
-   Upload a new file
-   Change permission of a file
-   View a file
-   Generate thumbnails for images

You will be guided step by step for building it, but you have some freedoms of implementation, split in more files etc... (`utils` folder will be your friend)

Of course, this kind of service already exists in the real life - it's a learning purpose to assemble each piece and build a full product.

Enjoy!

Resources
---------

**Read or watch**:

-   [Node JS getting started](https://alx-intranet.hbtn.io/rltoken/kZHDWCu20EsKxKzi51yWeg "Node JS getting started")
-   [Process API doc](https://alx-intranet.hbtn.io/rltoken/uYPplj2cPK8pcP0LtV6RuA "Process API doc")
-   [Express getting started](https://alx-intranet.hbtn.io/rltoken/SujfeWKCWmUMomfETjETEg "Express getting started")
-   [Mocha documentation](https://alx-intranet.hbtn.io/rltoken/FzEwplmoZiyGvkgKllZNJw "Mocha documentation")
-   [Nodemon documentation](https://alx-intranet.hbtn.io/rltoken/pdNNTX0OLugbhxvP3sLgOw "Nodemon documentation")
-   [MongoDB](https://alx-intranet.hbtn.io/rltoken/g1x7y_3GskzVAJBTXcSjmA "MongoDB")
-   [Bull](https://alx-intranet.hbtn.io/rltoken/NkHBpGrxnd0sK_fDPMbihg "Bull")
-   [Image thumbnail](https://alx-intranet.hbtn.io/rltoken/KX6cck2nyLpQOTDMLcwxLg "Image thumbnail")
-   [Mime-Types](https://alx-intranet.hbtn.io/rltoken/j9B0Kc-4HDKLUe88ShbOjQ "Mime-Types")
-   [Redis](https://alx-intranet.hbtn.io/rltoken/nqwKRszO8Tkj_ZWW1EFwGw "Redis")

Learning Objectives
-------------------

At the end of this project, you are expected to be able to [explain to anyone](https://alx-intranet.hbtn.io/rltoken/88vbnogJmkEoxqu-6wAXEw "explain to anyone"), **without the help of Google**:

-   how to create an API with Express
-   how to authenticate a user
-   how to store data in MongoDB
-   how to store temporary data in Redis
-   how to setup and use a background worker

Requirements
------------

-   Allowed editors: `vi`, `vim`, `emacs`, `Visual Studio Code`
-   All your files will be interpreted/compiled on Ubuntu 18.04 LTS using `node` (version 12.x.x)
-   All your files should end with a new line
-   A `README.md` file, at the root of the folder of the project, is mandatory
-   Your code should use the `js` extension
-   Your code will be verified against lint using ESLint

Provided files
--------------

### `package.json`

Click to show/hide file contents

### `.eslintrc.js`

Click to show/hide file contents

### `babel.config.js`

Click to show/hide file contents

Don't forget to run `$ npm install` when you have the `package.json`

# <<------------READTHIS ----------------->>
- This exercise's objectives are to give you some experience writing asynchronous APIs that interact with databases like MongoDb or Redis. You'll also learn about

[![Coverage Status](https://coveralls.io/repos/github/B3zaleel/alx-files_manager/badge.svg?branch=main)](https://coveralls.io/github/B3zaleel/alx-files_manager?branch=main)

- A simple file management API built with Express, MongoDB, Redis, Bull, and Node.js.

## Requirements

### Applications

+ Node.js
+ Yarn (the package manager/resource negotiator)

### APIs

+ A Google API should be created with at least an email sending scope and a valid URL (e.g.; `http://localhost:5000/`) should be one of the redirect URIs. The `credentials.json` file should be stored in the root directory of this project.

### Environment Variables

The required environment variables should be stored in a file named `.env` and each line should have the format `Name=Value`. The table below lists the environment variables that will be used by this server:

| Name | Required | Description |
|:-|:-|:-|
| GOOGLE_MAIL_SENDER | Yes | The email address of the account responsible for sending emails to users. |
| PORT | No (Default: `5000`)| The port the server should listen at. |
| DB_HOST | No (Default: `localhost`)| The database host. |
| DB_PORT | No (Default: `27017`)| The database port. |
| DB_DATABASE | No (Default: `files_manager`)| The database name. |
| FOLDER_PATH | No (Default: `/tmp/files_manager` (Linux, Mac OS X) & `%TEMP%/files_manager` (Windows)) | The local folder where files are saved. |

## Installation

+ Clone this repository and switch to the cloned repository's directory.
+ Install the packages using `yarn install` or `npm install`.

## Usage

Start the Redis and MongoDB services on your system and run `yarn start-server` or `npm run start-server`.

## Tests

+ Create a separate `.env` file for the tests named `.env.test` and store the value of the environment variables for the testing event in it.
+ Run `yarn test` or `npm run test` to execute the E2E tests.

## Documentation

+ TODO: Generate OpenAPI documentation with [**apidoc**](https://www.npmjs.com/package/apidoc).
