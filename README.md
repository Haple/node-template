<h1 align="center">
    Node Template
</h1>

<h4 align="center">
  Template backend for NodeJS.
</h4>
<p align="center">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/haple/node-template.svg">

  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/haple/node-template.svg">

  <!--FALTA COLOCAR A QUALIDADE DE CÓDIGO-->

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/haple/node-template.svg">
  <a href="https://github.com/haple/node-template.svg/commits/master">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/haple/node-template.svg">
  </a>

  <a href="https://github.com/haple/gympoint-backend.svg/issues">
    <img alt="Repository issues" src="https://img.shields.io/github/issues/haple/node-template.svg">
  </a>

  <img alt="GitHub" src="https://img.shields.io/github/license/haple/node-template.svg">
</p>

<p align="center">
  <a href="#technologies">Technologies</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#requirements">Requirements</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#install">Install</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#configure">Configure</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#running">Running</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#debug">Debug</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#root-config-files">Root config files</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#license">License</a>

</p>


## Technologies

This project was developed with the following technologies:

-  [VS Code](https://code.visualstudio.com/) with [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
-  [Node.js](https://nodejs.org)
-  [Express](https://expressjs.com/)
-  [nodemon](https://nodemon.io/)
-  [Sucrase](https://github.com/alangpierce/sucrase)
-  [Docker](https://www.docker.com/docker-community)
-  [Sequelize](http://docs.sequelizejs.com/)
-  [PostgreSQL](https://www.postgresql.org/)
-  [node-postgres](https://www.npmjs.com/package/pg)
-  [JWT](https://jwt.io/)
-  [Multer](https://github.com/expressjs/multer)
-  [Bcrypt](https://www.npmjs.com/package/bcrypt)
-  [Yup](https://www.npmjs.com/package/yup)
-  [date-fns](https://date-fns.org/)
-  [DotEnv](https://www.npmjs.com/package/dotenv)
<!-- -  [Youch](https://www.npmjs.com/package/youch) -->
<!-- -  [Sentry](https://sentry.io/) -->
<!-- -  [Bee Queue](https://www.npmjs.com/package/bcrypt) -->
<!-- -  [Nodemailer](https://nodemailer.com/about/) -->
<!-- -  [Redis](https://redis.io/) -->
<!-- -  [MongoDB](https://www.mongodb.com/) -->
<!-- -  [Mongoose](https://mongoosejs.com/) -->

---
## Requirements

For development, you will only need Node.js and a node global package, Yarn, installed in your environment.

### Node
- #### Node installation on Windows

  Just go on [official Node.js website](https://nodejs.org/) and download the installer.
Also, be sure to have `git` available in your PATH, `npm` might need it (You can find git [here](https://git-scm.com/)).

- #### Node installation on Ubuntu

  You can install nodejs and npm easily with apt install, just run the following commands.

      $ sudo apt install nodejs
      $ sudo apt install npm

- #### Other Operating Systems
  You can find more information about the installation on the [official Node.js website](https://nodejs.org/) and the [official NPM website](https://npmjs.org/).

If the installation was successful, you should be able to run the following command.

    $ node --version
    v8.11.3

    $ npm --version
    6.1.0

If you need to update `npm`, you can make it using `npm`! Cool right? After running the following command, just open again the command line and be happy.

    $ npm install npm -g

###
### Yarn installation
  After installing node, this project will need yarn too, so just run the following command.

      $ npm install -g yarn

### Docker
  Docker is used to handle the project resources, like database and queues services, at development time.
- [Docker installation on Windows](https://docs.docker.com/toolbox/toolbox_install_windows/)
- [Docker installation on Ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [Docker installation on other OS](https://docs.docker.com/install/linux/)

---

## Install

    $ git clone https://github.com/haple/node-template
    $ cd node-template
    $ yarn install

  - ### Install database
    Using docker, run the following command to install the database:
    ```
    sudo docker run -e 'POSTGRES_PASSWORD=UmaSenhaMuitoBoa' \
    -e 'POSTGRES_DB=node-template-db'\
    -p 5432:5432 --name node-template-db \
    -d postgres

    ```


## Configure

Open `./src/config/database.js` then edit it with your database settings. You will need:

- A host;
- A username;
- A password;
- A database;

## Running

    $ yarn dev

## Debug
First run the following:

    $ yarn dev:debug

Next step, go to debug tab on VS Code (ctrl + shift + D) and start debugging.


## Root config files

  ### .editorconfig
  Even whether your team of devs work with other code editors than not VS Code they this file preserve some code style configs.

  ### .eslintrc.js
  Used together with ESLint VS Code extension. ESLint statically analyzes your Javascript code to quickly find problems, which can be automatically fixed in most cases. Also used to force a code style in a dev team.

  ### .gitignore
  The files and folders listed in this file are ignored by git. Folders like *node_modules* and environment files are good exemple of things that should not be in version control.

  ### .prettierrc
  Used to custom the Prettier code style configs.

  ### .sequelizerc
  Used to configure common folders used by Sequelize (database orm).

  ### nodemon.json
  Used to register the Sucrase (ES5 transpiler) dependency to the lifecycle of Nodemon.

  ### .vscode/launch.json
  Config to enable NodeJS debug on VS Code.

## License
This project is under the MIT license. See the [LICENSE](https://github.com/haple/node-template/blob/master/LICENSE) for more information.

<!-- ## Simple build for production

    $ yarn build -->


