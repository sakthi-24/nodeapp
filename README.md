# Node Hello World

Simple node.js app that servers "Hello World"

Great for testing simple deployments on Cloud

## Step 1: Install NodeJS and NPM using nvm
Install node version manager (nvm) by typing the following at the command line.

```bash
sudo su -
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
```
Activate nvm by typing the following at the command line.

```bash
. ~/.nvm/nvm.sh
```

Use nvm to install the latest version of Node.js by typing the following at the command line.

```bash
nvm install node
```

Test that node and npm are installed and running correctly by typing the following at the terminal:

```bash
node -v
npm -v
```

## Step 2: Install Git and clone repository from GitHub
To install git, run below commands in the terminal window:

```bash
sudo apt-get update -y
sudo apt-get install git -y
```

Just to verify if system has git installed or not, please run below command in terminal:
```bash
git -v
```

This command will print the git version in the terminal.

Run below command to clone the code repository from Github:

```bash
git clone https://github.com/sakthi-24/nodeapp.git
```

Get inside the directory and Install Packages

```bash
cd nodeapp
npm install
```

Start the application
To start the application, run the below command in the terminal:

```bash
npm start
```
Go to your public ip address to verify whether it is sucessfully running or not.

PM2 is a daemon process manager that will help you manage and keep your application online. 
install pm2 with the npm command

```bash
npm install pm2 -g
```

 use pm2 to start our index.js application with the command below

```bash
pm2 start index.js --watch
```

Anytime there’s a changes in the code base, pull it to your local repository using git pull command.
Restart pm2 using the command below

```bash
pm2 restart index.js
```

CLEAN UP
  
Stop the running application using pm2 stop <application name>
```bash
pm2 stop index
```

 Kill the pm2 process by running
 ```
 pm2 kill
 ```

Exit from the instance by running the exit command.
