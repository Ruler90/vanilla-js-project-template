# Vanilla JS Project Template

This template can help you quickly start writing your Vanilla JS project and then bundle it with Webpack (you can use JS modules or import .css files into .js files too).

### Quick start:

1. Download this folder and make it your local repo.

2. Use ```npm install``` to install all dependencies listed in package.json.

3. Use my ESLint configuration file (I'm using airbnb styleguide) or delete it and create new.

4. You are ready to go.

6. To start webpack-dev-server, use ```npm run start```  
To bundle, minify and uglify all js and css code, use ```npm run build```

### Detailed start guide:

**1. Download this folder and make it your local repo.**

**2. Delete package.json and package-lock.json files and then use:**
```
npm init
npm install --save-dev @babel/core @babel/cli @babel/preset-env babel-loader css-loader style-loader webpack webpack-cli webpack-dev-server
```

**3. Add scripts to package.json file:**
```
"start": "webpack-dev-server --mode development",
"build": "webpack --mode production --watch"
```

**4. ESLint:**
```
npm install --save-dev eslint babel-eslint
```
Create ESLint config file and add parser in .eslintrc:
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
