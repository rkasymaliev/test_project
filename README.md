# test_project by Ruslan Kasymaliev
Task: using one docker-compose file, raise the structure of three services:

1. PostgreSQL is a database. It must be possible to connect to this database from the host system. Register a named volume for data storage. Add user, password, database to docker-compose.
2. Write a Dockerfile for [node.js application](https://nodejs.org/en/docs/guides/getting-started-guide/). Requirements:
    - It is necessary to copy all files from the shared directory to the built docker image, except for the node_modules directory and its contents
    - To install all dependencies, you need to run the `npm install` command
    - The application must start when the container starts. Command to start application `npm start`
3. The third service is Nginx. Nodejs application is listening on port 3000. The third service needs to raise a container with nginx, which will proxy connections from port 80 in the host system to port 3000 of NodeJS applications
