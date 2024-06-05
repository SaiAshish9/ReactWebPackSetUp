Steps:

1. npm init -y
2. npm install react react-dom
3. npm install --save-dev webpack webpack-cli webpack-dev-server
4. npm install --save-dev @babel/core @babel/preset-env @babel/preset-react babel-loader
5. Create a file named .babelrc in the root of your project where we can define various presets
6. Create a file named webpack.config.js in the root of your project where we can define module rules for various loaders, plugins, devServer config, server port, enable hot reloading, live reloading, entry point and path of the build output.
7. mkdir src public
8. touch src/index.js src/App.js public/index.html src/App.css
9. const root = ReactDOM.createRoot(document.getElementById("root"));
   root.render(
   <React.StrictMode>
   <App />
   </React.StrictMode>
   );
10. <body>
      <div id="root"></div>
    </body>

11. npm start
12. npm run build

