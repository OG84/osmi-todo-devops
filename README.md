# OSMI Thodo Devops

This repository contains all files to automatically start and stop the Thodo stack.

## Installation

Please checkout all of the following repositories ...

https://github.com/OG84/osmi-todo-devops  
https://github.com/OG84/osmi-todo-frontend  
https://github.com/OG84/osmi-todo-api  

... into a shared folder, e.g.:

\- osmi-todo  
&nbsp;&nbsp;|- osmi-todo-devops  
&nbsp;&nbsp;|- osmi-todo-frontend  
&nbsp;&nbsp;|- osmi-todo-api  

## Start in development mode

The development mode starts up the following services:

- NEO4J Graph Database

Frontend and Api should be started seperately.

Type `yarn docker-run:dev` to compose the dev stack.  
For starting the frontend and api in dev mode please see the individual READMEs.

## Start in production mode

The production mode starts up all required services:

- NEO4J Graph Database
- Thodo nest.js Api
- Thodo Angular Frontend

Type `yarn docker-run` to compose the production stack.  
The Application can now be accessed on port 80.

The startup takes a couple of minutes, because frontend and api images are rebuild each time.

If running the production mode on your local machine, the frontend is accessing the backend on `http://thodo.th-brandenburg.de:3000/api/v1/todos`, so it's not accessing your local api.

## Important

Make sure that every repository is up to date.

Run `git pull` in each of them.