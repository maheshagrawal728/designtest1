# Testing as a Service Nodejs Application
A containerized and distributed Testing as a service application for VMC product


## Prerequisites
- Install git
- Cloining the repo:
	Please follow the steps below to setup an SSH key for your Stash account:
	- Generate an SSH key on your local machine [(Refer SSH keys section)](https://wiki.eng.vmware.com/Build/DBC)
	- In Stash, click your user icon in the top right corner and then click on Manage Account
	- Click on the SSH keys link on the left and then click on the Add key button
	- Copy and paste the public key (which is usually in the file ~/.ssh/id_rsa.pub) that you generated in step 1 and then click on Add key
	- Change into your development directory, and clone the remote Git repository by running the command below:
	- git clone ssh://git@stash.eng.vmware.com:7999/ss/eust.git  [(Repo Link)](https://stash.eng.vmware.com/stash/projects/SS/repos/eust/browse)


- Install databse mysql:
	- Installing mysql using Homebrew: brew install mysql
	- Check version: mysql -V
	- load and start the MySQL service : brew services start mysql.
	- Check of the MySQL service has been loaded : brew services list
	- Create Username and password: mysqladmin -u root password 'ca$hc0w'
	- Enter Mysql: mysql -u root -p
	- Source the project database information: mysql> source PATH/eust/node/database/setup.sql;

	- Edit mysql config file to allow all traffic.
	- mysql --help, look for my.cnf file location and edit the file with below details:
		- bind-address=*
		- Comment line skip-networking
		- restart the service.
		- location of the condif file: /etc/my.cnf /etc/mysql/my.cnf /usr/local/etc/my.cnf ~/.my.cnf 

- Need node and npm. [(Refer)](https://nodejs.org/en/download/package-manager/)
- Docker installed and have access to loop/eust/goat docker image
	- If docker Image not available build them:
		- Build: 
    			- cd PATH/eust/docker/goat, docker build -t docker-goat-image .
    			- cd PATH/eust/docker/eust, docker build -t docker-eust-image .


## Instructions for Command-line
#### Building:
 - cd path_to_node/
 - npm install
     Description: Since package.json is present in the restapp directory.
     Above command will create a folder callled node_modules and
     Install all the dependencies required for the app.
     
#### Running:
 - Change server address if needed, which includes IP and PORT
 @path_to_node/conf/config.json, @path_to_node/public/lib/js/logic.js
 - Change database details if needed, @path_to_node/database/dbConfig.json
 - npm start
 Use browser with server adderss provided to use the application i.e. http://10.52.76.120:3000/ or Use curl and other utilities.
 
#### Development:
 - Modules installation: Install node modules using npm and save it in package.json. i.e.  npm install xx --save
 - Exposing Rest api: refer @path_to_node/controllers/example.js


## List of APIs Exposed
#### API for login -- /users/login
- Example: curl -X POST -H "Accept: application/json" -H "Content-Type: application/json" -d '{ "user":"test", "pass":"test"}' http://10.52.76.120:3000/users/login

#### API for signup -- /users/signup
- Example: curl -X POST -H "Accept: application/json" -H "Content-Type: application/json" -d '{ "user":"test", "pass":"test"}' http://10.52.76.120:3000/users/signup

#### API for loop test -- /loop
- Example: curl -X POST -H "Accept: application/json" -H "Content-Type: application/json" -d '{ "loopRunName":"testing","loopRunUser":"test", "loopRunPassword":"test"}' http://10.52.76.120:3000/loop

#### API for loop test -- /loop
curl -X POST -H "Accept: application/json" -H "Content-Type: application/json" -d '{"username":"mahesh","userpass":"mahesh"}' http://10.52.76.120:3000/loop/result






# designtest1
designtest1
hh1
new
nn  
latest changes


# Testing as a Service Nodejs Application
A containerized and distributed Testing as a service application for VMC product


## Prerequisites
- Need node and npm. [(Refer)](https://nodejs.org/en/download/package-manager/)
- Docker installed and have access to loop/eust/goat docker image


## Instructions for Command-line
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


## Instructions for Eclipse
To be done.


## Instructions for Intellij
To be done.


## List of APIs Exposed
#### API for login -- /users/login
- Example: curl -X POST -H "Accept: application/json" -H "Content-Type: application/json" -d '{ "user":"test", "pass":"test"}' http://10.52.76.120:3000/users/login

#### API for signup -- /users/signup
- Example: curl -X POST -H "Accept: application/json" -H "Content-Type: application/json" -d '{ "user":"test", "pass":"test"}' http://10.52.76.120:3000/users/signup

#### API for loop test -- /loop
- Example: curl -X POST -H "Accept: application/json" -H "Content-Type: application/json" -d '{ "loopRunName":"testing","loopRunUser":"test", "loopRunPassword":"test"}' http://10.52.76.120:3000/loop
