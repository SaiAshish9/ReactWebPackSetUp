Here's how we can create a new React project from scratch by manually configuring Webpack and Babel, bypassing the use of create-react-app. Additionally, we'll explore how create-react-app sets up the configuration for Webpack and the Webpack Dev Server.

Steps for Creating a React App from Scratch Without CRA:

1. Create Project Directory:
mkdir Project_Directory && cd Project_Directory
2. Initialize npm:
npm init -y
3. Install React and React DOM:
npm i react react-dom
4. Install Webpack and Webpack CLI:
npm i --save-dev webpack webpack-cli webpack-dev-server
5. Install Babel:
npm i --save-dev @babel/core @babel/preset-env @babel/preset-react babel-loader
6. Install HTML Webpack Plugin:
npm i --save-dev html-webpack-plugin
7. Install CSS Loader and Style Loader:
npm i --save-dev css-loader style-loader
8. Configure Babel: 
Create a .babelrc file and define the following presets:
"@babel/preset-env", "@babel/preset-react"
9. Configure Webpack: 
Create a webpack.config.js file to define module rules for various loaders (CSS, style, and JS), plugins like HtmlWebpackPlugin, devServer configuration, server port, enable hot/live reloading, and specify the entry point and path of the build output.
10. Set Up Project Structure: 
Create src and public directories.
11. Create public/index.html: This file should contain a div with id="root". In src/index.js, define the entry point where ReactDOM.createRoot renders the App component using that id.
12. Add Scripts to package.json: Add the following scripts:
"scripts": {
 "start": "webpack serve --mode development",
 "build": "webpack --mode production"
}
13. Execute npm run start or yarn start to run the server.

How Create React App (CRA) Configures Webpack:

CRA uses a package called react-scripts to manage the setup of the development environment, including the configuration of Webpack and the Webpack Dev Server.

When you execute the create-react-app command, it installs react, react-dom, and react-scripts along with a CRA template.

Running npm start triggers the following steps:

1. Entry Point: The start script in package.json executes the react-scripts start command.
2. React-Scripts: Inside node_modules/react-scripts/scripts/start.js, the script initializes the Webpack Dev Server
3. Webpack Configuration: The development Webpack configuration is located in node_modules/react-scripts/config/webpack.config.js. This configuration includes:
4. Entry points
5. Loaders for processing JS, CSS, and other files.
6. Plugins for various development functionalities.
7. Dev Server Setup: The Webpack Dev Server config is included in node_modules/react-scripts/config/webpackDevServer.config.js.

If you need to customize the Webpack config provided by CRA, you can use tools like react-app-rewired.
