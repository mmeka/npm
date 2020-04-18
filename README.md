# npm

# npm init default configuration
npm config set init-author-name "<author_name>"
npm set init-author-name "<author_name>"  # "npm config set" or "npm set" would do the same
npm config delete init-author-name

Initialize the npm project with defaults using the following command
npm init --yes   (remember to delete the package.json before running "npm init" command)


# Installation of modules
npm install (-g) <module_name> --o save     # save will add the dependency to the package.json file
npm i -g browserify


# Popular modules
https://www.npmjs.com has all the modules
Lodash (for arrays sorting and looping; setting timeouts and delays)

# Importing modules
const _ = require('lodash')  (Here, underscore is converntional for Lodash)


# Lodash example
const numbers = [10,20,40,30];
_.each(numbers,function(number,index){
 // print each number
});
