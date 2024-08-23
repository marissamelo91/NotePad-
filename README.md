# NotePad- PWA
NotePad- is a Progressive Web App (PWA) designed for taking and managing notes offline. This application leverages Webpack for bundling and integrates various technologies to provide a smooth offline experience.

## Table of Contents
[Features](#features)
[Installation](#installation)
[Usage](#usage)
[Configuration](#configuration)
[Database](#database)
[ServiceWorker](#service-worker)


## Features
* Offline note-taking capability. 
* Progressive Web App (PWA) with installable options.
* Uses IndexedDB for data storage.

## Installation
* Clone the repository: git clone https://github.com/yourusername/notepad-pwa.git 
* Navigate to the project directory: cd notepad-pwa 
* Install dependencies: npm install 

## Usage
Start the development server: npm start 
This will start the Webpack development server and you can view the app at http://localhost:8080.
Build for production: npm run build


## Configuration
The webpack.config.js file is configured to:
* Bundle JavaScript files (index.js and install.js). <br>
* Use HtmlWebpackPlugin to generate the index.html file. <br>
* Use WebpackPwaManifest to create a manifest file for PWA.<br>
* Use InjectManifest from workbox-webpack-plugin for service worker management.<br>
* Handle CSS files and transpile JavaScript using Babel.<br>

Service Worker <br>
The service worker is configured using Workbox:<br>
* InjectManifest plugin injects custom service worker code from src-sw.js.<br>

PWA Manifest<br>
The PWA manifest file is configured to:<br>
* Define app name, short name, and description.<br>
* Specify app icon sizes and location.<br>

## Database
The application uses IndexedDB to store and retrieve notes. <br>
Methods
* putDb(content): Stores content in the IndexedDB under the object store jate.
* getDb(): Retrieves all content from the IndexedDB.

Initialization
The database is initialized with an object store named jate using the idb library.

## Service Worker
The application uses a service worker to cache assets and handle offline functionality. It also handles the installation process and prompts the user to install the PWA when applicable.

Install Button Logic
* Event Listener: Listens for the beforeinstallprompt event to show the install button.
* Click Event: Shows the install prompt and handles the installation process.
* App Installed Event: Clears the prompt after the app is installed.

## Credits
* Class Lectures
* Tutor Session
* Classmates - Thinh Nguyen and Faiza Haque
* AI Tools - CHATGPT, Amazon Q, and Copilot
