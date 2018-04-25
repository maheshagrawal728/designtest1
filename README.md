# designtest1
designtest1
hh1
new
nn  
latest changes


# Testing as a Service Nodejs Application

## Prerequisites

 1. Need node and npm
 
 [Refer:](https://nodejs.org/en/download/package-manager/)
 
 2. Docker installed and have access to loop/eust/goat docker image

## Buildin and Running APP from Command-line

#### Building:
 - cd path_to_node/
 - npm install
     Description: Since package.json is present in the restapp directory.
     Above command will create a folder callled node_modules and
     Install all the dependencies required for the app.
     
#### Running:
 - Change server address if needed, which includes IP and PORT
 @path_to_node/conf/config.json, @path_to_node/public/lib/js/logic.js
 - npm start
 Use browser with server adderss provided to use the application i.e. http://10.52.76.120:3000/ or Use curl and other utilities.
 
#### Development:
 - Modules installation: Install node modules using npm and save it in package.json. i.e.  npm install xx --save
 - Exposing Rest api: refer @path_to_node/controllers/example.js
 
## Buildin and Running APP from Eclipse

TODO

## Buildin and Running APP from Intellij

TODO

## List of APIs Exposed

#### API for login -- /users/login
- Example: curl -X POST -H "Accept: application/json" -H "Content-Type: application/json" -d '{ "user":"test", "pass":"test"}' http://10.52.76.120:3000/users/login

#### API for signup -- /users/signup
- Example: curl -X POST -H "Accept: application/json" -H "Content-Type: application/json" -d '{ "user":"test", "pass":"test"}' http://10.52.76.120:3000/users/signup

#### API for loop test -- /loop
- Example: curl -X POST -H "Accept: application/json" -H "Content-Type: application/json" -d '{ "loopRunName":"testing","loopRunUser":"test", "loopRunPassword":"test"}' http://10.52.76.120:3000/loop



