# node-project-deployment

Node.js REST API built with **Express** and **MongoDB (Mongoose)**.

## Tech Stack
- Node.js + Express
- MongoDB + Mongoose
- CORS enabled

## Project Structure (high level)
- `server.js` – Express app entrypoint, DB connection, routes registration
- `app/` – application code (models, routes, controllers, etc.)

## Prerequisites
- Node.js (LTS recommended)
- npm
- A running MongoDB instance (local or cloud)

## Install
```bash
npm install
```

## Configure Environment
This project uses `process.env.PORT` (defaults to **8080** in `server.js`).

You also need to configure the MongoDB connection used by:
```js
const db = require("./app/models");
db.mongoose.connect(db.url, ...)
```

Find where `db.url` is defined (typically under `app/models/index.js`) and set it to your MongoDB connection string, or update the code to read it from an environment variable such as `MONGODB_URI`.

Example (recommended):
- `MONGODB_URI=mongodb://localhost:27017/mydb`
- `PORT=8080`

## Run (Development)
```bash
node server.js
```

Server will start on:
- `http://localhost:8080`
