# npm

# npm init default configuration
npm config set init-author-name "<author_name>"
npm set init-author-name "<author_name>"  # "npm config set" or "npm set" would do the same
npm config delete init-author-name

Initialize the npm project with defaults using the following command
npm init --yes   (remember to delete the package.json before running "npm init" command)

# Installation of modules
npm install (-g) (--o) (--save|--save-dev) <module_name>(@<version_number>)     # save will add the dev dependency to the package.json file
npm i -g browserify nodemon (more than one module can be installed at a time)

NOTE: Globally installed modues are found at the location using command "npm root -g".

# Listing modules
npm list (--depth 0)

# Removing modules
npm uninstall <module_name> (--save-dev) (removes from node_modules as well as from package.json)
npm remove <module_name> (does same thing and has same options as that of "npm uninstall")
npm rm <module_name> (does same thing and has same options as that of "npm uninstall")
How to uninstall a specific version only??

# Updating modules
npm update
npm update <module_name>

# Popular modules
https://www.npmjs.com has all the modules
Lodash (for arrays sorting and looping; setting timeouts and delays)
Gulp (for minification of JavaScript files; compiling Sass files)

# Starting application
1) Using Node
  "main": "index.js",
   "scripts": {
     "start": "node index.js"
   }
   
   File name can be index.js or app.js or anything else. Just mention in both places
   
   > npm start
   OR
   > npm run start

2) Using Node live-server
  "main": "index.js",
   "scripts": {
     "start": "node index.js",
     "server" :"live-server"
   }
   
   File name can be index.js or app.js or anything else. Just mention in both places
   
   > npm run server

# Live server examples
1) Nodemon (continuously look for any changes in the JS files; restarts the Node server when required; global installation;
To run, use command "nodemon" from any of the Node project. This is good for Express, Web server)
2) Install live-server plug-in under Microsoft Visual Studio Code. Use the Live-Server icon on the status bar of the editor.
3) Install live-server
npm install live-server -g (loads up localhost with index.html)

# Importing modules
1) const _ = require('lodash')  (Here, underscore is converntional for Lodash)
2) import { $ } from 'jQuery';


# Executing JavaScript
Using Node,
> node <JS_file_name_without_JS_extension>
Using Browerify or Webpack

# Saving to repository
Ignore Node_modules folder from committing.

# Retrieving from repository
> npm install (--production) ("--production" option downloads only regular dependencies, not dev-dependencies;this will get required modules from a computer with node installed. How to know what node version to use from the recipient computer?)

# Lodash example
const numbers = [10,20,40,30];
_.each(numbers,function(number,index){
 // print each number
});

# Package.json
Note that version menetioned as "^3.3.0" will resolve dependencies, fetching the latest minor versions or any patches. "~4.17.4" will fetch only the bug fixes aka patches. "*" isn't recommended for production as it would fetch major versions too.

# Publishing modules
1) Create npm account; verify email.
2) > npm adduser 
3) In JS file, have the line added
  module.exports.<module_name> = <JS_function_name>;
4) Create GIT repo and commit the code
5) > npm publish
6) Search in npmjs.org
