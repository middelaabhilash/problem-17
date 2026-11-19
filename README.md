# Problem Overview

This project is a small Node.js + Express challenge. The goal is to create a simple web server that responds correctly to a request and then submit the completed project for evaluation.

## What the app is supposed to do

When the server runs, a request to the root route `/` should return:

`Be a Coding Ninja`

This is the core requirement of the problem.

## Included files

- `index.js`  
  Contains the Express app setup. This is the main file where the solution is implemented.

- `server.js`  
  Starts the server on port `3000`.

- `upload_project.js`  
  Packages the project into a zip file, excluding `node_modules`, and uploads it to the Coding Ninjas submission API using a JWT token.

- `package.json`  
  Lists project dependencies and scripts.

## Setup

1. Install dependencies:
   ```bash
   npm install
   ```

2. Start the server:
   ```bash
   node server.js
   ```

3. Open the app in a browser or use curl:
   ```bash
   curl http://localhost:3000/
   ```

Expected output:
```text
Be a Coding Ninja
```

## How the submission works

The `upload_project.js` script is used to submit the project for evaluation. It:

- creates a zip of the project files
- ignores `node_modules`
- checks the zip size
- sends the file to the Coding Ninjas API with a JWT token

Usage:
```bash
node upload_project.js <JWT_TOKEN>
```

Example:
```bash
node upload_project.js YOUR_JWT_TOKEN_HERE
```

## Important notes

- The main goal is to fix and complete the Express server logic.
- Do not change `upload_project.js` unless the instructions explicitly say to do so.
- This is a basic exercise to practice building a simple API server and understanding project submission flow.

## Final objective

Build the server so that:

- it runs without errors
- the `/` route returns `Be a Coding Ninja`
- the project can be submitted successfully through the provided upload script
