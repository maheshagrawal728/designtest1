VMC INTERNAL SRE
================
This cli is meant to support and remediate issues for internal vmc customers and directed towards making the internal-sre a self service process. 
It will have the capabilities listed in the following confluence-
https://confluence.eng.vmware.com/pages/viewpage.action?spaceKey=DRMTEAM&title=VMC+Reaper+CLI
 
Build & Run (Note: Installation instructions are for Mac OS X having bash shell and Homebrew)
-----------
Please follow the steps below to clone stash based project using SSH::

    1. Generate an SSH key on your local machine (https://confluence.atlassian.com/bitbucketserver/creating-ssh-keys-776639788.html)

    2. In Stash, click your user icon in the top right corner and then click on Manage Account

    3. Click on the SSH keys link on the left and then click on the Add key button

    4. Copy and paste the public key (which is usually in the file ~/.ssh/id_rsa.pub) that you generated in step 1 and then click on Add key

    5. Change into your development directory, and clone the remote Git repository by running the command below:

    git clone ssh://git@stash.eng.vmware.com:7999/ss/vmc-internal-sre.git


Please follow the steps below to clone stash based project using HTTPS::

    git clone https://username@stash.eng.vmware.com/stash/scm/ss/vmc-internal-sre.git


Please run following command to install cli dependencies and activate it in the current terminal::

    cd PATH_TO_CLI/vmc-internal-sre/
    source init-cli.sh


Please run following command to manually activate cli in another terminal::

    cd PATH_TO_CLI/vmc-internal-sre/
    source activate-cli.sh


Please run following command to deactivate cli in current terminal::

    pyenv deactivate


Please run following command to uninstall or delete cli from the system::

    pyenv uninstall isre


If you'd like to run all tests for this project, you would run the following command::

    python setup.py test


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
