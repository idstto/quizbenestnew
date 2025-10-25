# Development

## Install Node.js and Nest.js

1. Download Node.js from [nodejs.org](https://nodejs.org/en/download/current).
2. Run and install the downloaded file.
3. Type this command below on your terminal to install the Nest.js CLI (Command Line Interface).

```sh
npm i -g @nestjs/cli

```

## Generate a New Project

Run this command on your terminal:

```sh
nest new <project_name>
# e.g. nest new quizbenest

```

## Run the Project

1. Run this command to go to the project directory:

```sh
cd <project_directory>
# e.g.:
# cd quizbenest
# cd D:\projects\quizbenest # Windows
# cd ~/projects/quizbenest # Unix

```

2. Run this commmand to run the project:

```sh
npm run start:dev

```

## Test the API

1. Install [REST Client for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=humao.rest-client) or [Postman](https://www.postman.com/)

2. Create a New File with .http extension, e.g.: ./rest/user.http

3. Update the file content with these lines:

```text
### Test Root Endpoint

GET http://localhost:3000/

```

4. Send the Request, and it should get the response like this:

```sh
Hello World!

```

## Create a New Resource

1. Open a new terminal, and run this command:

```sh
nest generate resource <resource_name>
# e.g. nest generate resource features/users
# or
nest g res <resource_name>
# e.g. nest g res features/users

```

To test the command without generating the files, add **--dry-run**, e.g.:

```sh
nest g res features/users --dry-run

```

2. Add these lines to the .http file:

```text
### User Endpoint

GET http://localhost:3000/users

```
