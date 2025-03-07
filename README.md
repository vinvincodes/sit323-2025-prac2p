# SIT323-2025-Prac2P: Build Simple Node.js webserver

## Project overview

This task is serving a simple HTML by creating a web server with Node.js, this will use Express framework.

# Tool used

- Git & github
- vscode
- node.js & Express.js

# setup instructions

## Installing and Setup Git, Github, VSCode, and Node.JS

1. Install Git

- Download and Install: https://git-scm.com/ > Downloads > Install based on your OS

- open Git Bash, and check verify for installation

```
git -v
```

- if Git isn't update yet, you can update following this command: `git update`

2. Install Visual Studio Code (VScode)

- Download and Install the VSCode from this site: https://code.visualstudio.com/
- Once open VSCode, you can click open terminal on navigation bar, new terminal: or press `` ctrl + ` ``

3. Install Node.js

- Go to Node.js site: https://nodejs.org/en
- Download and install the _Latest Node.js LTS version_ for your OS
- Then click for execute it

- Once done installed, then verify the installation by running in terminal/command prompts:
  ```
  node -v
  npm -v
  ```
- If Node.js is installed correctly, it will display the latest version number

## Setup a GitHub Repository

1. Go to GitHub and create an account if you don’t have one: https://github.com/
2. Set up your repository

- Open GitHub once you've created account. Then,
- click _New Repository_ -> Name it: `sit323-2025-prac2p`
- Select _public_, and _Add a README_, then create the repo.
- copy your repo URL: `https://github.com/your-username/sit323-2025-prac2p`

## Setup a Local Project Folder

1. Open VScode and create a new folder in any path: `sit323-2025-prac2p`
2. Open the terminal in VS Code (`` Ctrl + `  ``) or git bash
3. Run these commands to initialise the project:

```
git init
git remote add origin https://github.com/your-username/sit323-2025-prac2p
git pull origin main

```

## Initilise Node.Js & Install Express.js

1. In your terminal/command prompt/git bash, navigate to your project foler:

```
cd any_Path/sit323-2025-prac2p
```

2. Initialised a node.js project -- to create a `package.json` file:

```
npm init -y
```

3. Install express.js -- to install the `package-lock.json` file

```
npm install express
```

## Create a Simple webserver using Express.js

1. Inside a folder, create a new file: `server.js`
2. Open `server.js` and add these code:

```
const express = require("express");
const app = express();
const port = 3000;

app.use(express.static("public"));

app.get("/", (req, res) => {
  res.sendFile(__dirname + "/public/index.html");
});

app.listen(port, () => {
  console.log(`Server running at http://localhost:${port}`);
});

```

## Create a Simple HTML page

1. Inside the folder, create a `public` folder.
2. inside `public` folder, create a new file: `index.html`
3. Add these HTML code:

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>My Node.js Simple Webserver</title>
  </head>

  <body>
    <h1>Welcome to My Express Server!</h1>
    <p>This page is delivered by Express.js.</p>
  </body>
</html>


```

## Testing your Webserver

1. Start the server on the terminal: `node server.js`
2. http://localhost:3000

## Push your code to GitHub

1. Run the following Git commands:

```
git add .
git commit -m "Node.js webserver Added"
git branch -M main
git push origin main

```

2. Go to your GitHub repo to check that your files have been uploaded: https://github.com/your-username/sit323-2025-prac2p
