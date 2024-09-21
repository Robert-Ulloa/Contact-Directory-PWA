# Contact Directory PWA

A Progressive Web App (PWA) for managing contact information. The app supports adding, removing, and storing contact details in an IndexedDB database and allows installation as a PWA. The app is built using Webpack, Express, IndexedDB, and Service Workers for offline functionality.
 ## Live Demo:

Contact Directory PWA on Render:
 https://contact-directory-pwa.onrender.com

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Build and Run](#build-and-run)
- [Technologies Used](#technologies-used)
- [Folder Structure](#folder-structure)
- [License](#license)

---

## Installation

Before running the app, ensure you have the following installed on your system:
- [Node.js](https://nodejs.org/) (version 14.x or higher)
- [npm](https://www.npmjs.com/) (comes with Node.js)

### Steps

1. Clone the repository to your local machine:

    ```bash
    git clone https://github.com/Robert-Ulloa/Contact-Directory-PWA
    ```

2. Navigate to the project directory:

    ```bash
    cd contact-directory-pwa
    ```

3. Install dependencies for both client and server:

    **In the root directory:**
    ```bash
    npm install
    ```

    **Navigate to the client folder:**
    ```bash
    cd client
    npm install
    ```

    **Navigate to the server folder:**
    ```bash
    cd ../server
    npm install
    ```

4. Return to the root directory:
    ```bash
    cd ..
    ```

---

## Usage

### Running in Development Mode

To start the app in development mode, which will run both the client and server with hot-reloading, follow these steps:

1. In the root directory, run the following command:

    ```bash
    npm run start:dev
    ```

2. Open your browser and navigate to:

    ```
    http://localhost:8080
    ```

### Running in Production Mode

To build and run the app in production mode:

1. **Build the Client**:

    In the root directory, run:

    ```bash
    npm run build
    ```

   This command bundles the client-side assets using Webpack and outputs them to the `dist/` folder.

2. **Start the Server**:

    After building, run:

    ```bash
    npm run start
    ```

   This will start the server in production mode, serving the bundled assets from the `dist/` folder.

3. Open your browser and navigate to:

    ```
    http://localhost:3000
    ```

---

## Features

- Add, delete, and view contact cards.
- Offline functionality with service workers and IndexedDB.
- Installable as a Progressive Web App (PWA).
- Full client-server architecture with Webpack for bundling.

---

## Build and Run

### Scripts in `package.json`:

- **Development Mode**:
  
  ```bash
  npm run start:dev
  ```

  Runs both the client and server concurrently with hot-reloading for development.

- **Production Build**:

  ```bash
  npm run build
  ```

  Bundles the client assets using Webpack and outputs them into the `dist/` directory.

- **Run Server in Production Mode**:

  ```bash
  npm run start
  ```

  Runs the Express server serving static files from the `dist/` directory.

- **Run Server Only**:

  ```bash
  npm run server
  ```

  Starts the Express server without building the client.

---

## Technologies Used

- **Frontend**:
  - HTML, CSS, JavaScript (ES6+)
  - Webpack (for bundling)
  - IndexedDB (for storing contact data locally)
  - Service Workers (for offline functionality)
  - Workbox (for registering the service worker)

- **Backend**:
  - Express.js (for serving the app and handling routes)

- **Build Tools**:
  - Webpack
  - Babel (for ES6+ transpilation)
  - CopyWebpackPlugin (to copy files like `src-sw.js` to `dist`)

---

## Folder Structure

```bash
.
├── client/               # Frontend code
│   ├── dist/             # Webpack output (bundled files)
│   ├── src/
│   │   ├── js/           # JavaScript files
│   │   └── css/          # Stylesheets
│   └── webpack.config.js # Webpack configuration
├── server/               # Backend code
│   ├── routes/           # API routes
│   └── server.js         # Express server
├── package.json          # Root package.json (coordinates client/server)
└── README.md             # This file
```

---

## License

This project is licensed under the MIT License.

---

### Mockup Section

> The application allows users to store and manage contacts. Users can add new contacts with name, home phone, cell phone, and email details. The app uses IndexedDB to store data, making it accessible even when offline. A service worker provides offline caching, and the app can be installed as a PWA.

