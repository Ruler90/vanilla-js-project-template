# Vanilla JS Project Template

This template can help you quickly start writing your Vanilla JS project and then bundle it with Webpack (you can use JS modules or import .css files into .js files too).

**Update 2020-07-22**  
Removed all dependencies so ```npm install``` won't work. If you install everything as described below, you'll get most recent version of every dependency.

### Start guide:

**1. Download this folder and make it your local repo.**

**2. Create package.json file and install dependencies:**
```
npm init
npm install --save-dev @babel/core @babel/cli @babel/preset-env babel-loader css-loader style-loader webpack webpack-cli webpack-dev-server
```

**3. Add two scripts to package.json file:**
```
"start": "webpack-dev-server --mode development",
"build": "webpack --mode production --watch"
```
To start webpack-dev-server, use ```npm run start```  
To bundle, minify and uglify all js and css code, use ```npm run build```

**4. ESLint:**
```
npm install --save-dev eslint babel-eslint
```
To use my ESLint configuration file:
```
npm install --save-dev eslint-config-airbnb
```
or you can delete it, create new ESLint config file and add parser in .eslintrc:
```
"parser": "babel-eslint"
```
More info about [babel-eslint](https://github.com/babel/babel-eslint)

**5. Helphul VS Code extensions:**
- Auto Rename Tag (by Jun Han)
- Beautify or Prettier
- Bracket Pair Colorizer (by CoenraadS)
- ESLint (by Dirk Baeumer)
- Git Graph (by mhutchie)
- Live Sass Compiler (by Ritwick Dey)
- Markdown Preview Github Styling (by Matt Bierner)
- Select Line Status Bar (by tomoki1207)

**6. If you want to see your app on other devices in your network:**
* In webpack.config.js in ```devServer``` change ```host: 'localhost'``` to your local IP number, e.g. ```host: '192.168.0.66'```.
* Open the browser in other device and type the same address, port, folder/file as you see when you start webpack-dev-server.
* If you use Windows 10, make sure your home network is set to private. If it's set to public you won't connect from other devices.
