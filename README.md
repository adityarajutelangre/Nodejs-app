Jenkins Node.js Web Application 🚀

A simple web application built with Node.js and Express.js. The application runs on port 3000 and displays a message on the home page. It is a beginner-friendly project for learning Node.js, GitHub, webhooks, and Jenkins CI/CD concepts.

1. Introduction 💡
This project creates a web server using Node.js and Express.js. When a user visits the home page (/), the server sends the following message:
Hiii from jenkins, added webhook, we are from 18 May Devops batch

The project can be used as a starting point for learning how application code can be stored in GitHub and later connected to Jenkins pipelines and webhook automation.

2. Objectives 🎯
- Create a web server using Node.js.
- Handle HTTP requests with Express.js.
- Display a message on the home page.
- Manage dependencies and the start command through package.json.
- Learn the basic concepts behind GitHub webhooks and Jenkins CI/CD.
- Explore deployment on a Linux server or AWS EC2.

3. Technologies Used 🛠️
Technology	Purpose
Node.js	Runs JavaScript on the server
Express.js	Handles HTTP requests and routes
JavaScript	Application programming language
npm	Installs and manages dependencies
Git	Tracks source-code changes
GitHub	Hosts the project repository
Jenkins	Optional CI/CD automation
GitHub Webhook	Optional event notification to Jenkins
AWS EC2	Optional application hosting
PM2	Optional Node.js process management


Note: The uploaded application files directly configure Node.js and Express.js. Jenkins, webhook automation, AWS EC2 deployment, and PM2 require separate setup.

4. Architecture Diagram 🏗️
CI/CD workflow (when configured)
Developer
   |
   v
Push Code to GitHub
   |
   v
GitHub Webhook
   |
   v
Jenkins Pipeline
   |
   +--> Install Dependencies / Tests
   |
   v
Deploy to Server (e.g., AWS EC2)
   |
   v
Restart Application (optional PM2)
Application runtime flow
User / Web Browser
        |
        | HTTP GET /
        v
Server (localhost:3000 or deployed host)
        |
        v
     Node.js
        |
        v
    Express.js
        |
        v
  Route: GET /
        |
        v
 res.send(message)
        |
        v
HTTP Response to Browser
The CI/CD workflow above describes a possible setup; it is not automatically created by the two application files.

5. Project Structure 📁
Nodejs-app/
├── app.js
├── package.json
└── README.md
- app.js — creates the Express application, defines the / route, and starts the server.
- package.json — defines project metadata, the start script, and the Express.js dependency.
- README.md — documents the project and how to run it.
A package-lock.json file may also be generated when dependencies are installed; commit it if it is part of your project.

6. Input 📥
Item	Value
URL (local)	http://localhost:3000/
HTTP method	GET
Route	/
Port	3000
Request body	Not required


Input Process
1. The user opens a browser.
2. The user visits http://localhost:3000/.
3. The browser sends an HTTP GET request to /.
4. Express.js handles the route.

7. Output 📤
Browser output
Hiii from jenkins, added webhook, we are from 18 May Devops batch
Terminal output
App listening at http://localhost:3000
The terminal message appears when the server starts. The browser message appears when the home page is requested.

8. How the Application Works ⚙️
1. require('express') loads Express.js.
2. express() creates the application.
3. The application uses port 3000.
4. app.get('/') defines the home-page route.
5. res.send() sends the configured text to the browser.
6. app.listen() starts the server and logs the local URL.

9. Installation and Local Setup 💻
Prerequisites
- Node.js and npm installed.
- Git installed (if cloning the repository).
Check your versions:
node --version
npm --version
git --version
Step 1: Clone the repository
git clone https://github.com/adityarajutelangre/Nodejs-app.git
cd Nodejs-app
Step 2: Install dependencies
npm install
Step 3: Start the application
npm start
The start script in package.json runs:
node app.js
Step 4: Open the application
Visit this URL in your browser:
http://localhost:3000/
To stop the server, press Ctrl + C in the terminal.

10. AWS EC2 Deployment (Optional) ☁️
These are general deployment steps; they are not configured by the uploaded files alone.
1. Launch a Linux EC2 instance.
2. Connect to the instance using SSH.
3. Install a supported Node.js version, npm, and Git using the package manager for your Linux distribution.
4. Clone the repository:
   git clone https://github.com/adityarajutelangre/Nodejs-app.git
   cd Nodejs-app
5. Install dependencies and start the application:
   npm install
   npm start
6. For direct testing, configure the EC2 security group to allow the required inbound port and ensure the server is reachable. For a more secure deployment, consider Nginx as a reverse proxy and HTTPS.
Use the actual public IP or DNS name of your instance when testing a deployed app. Do not use localhost from your personal computer to reach the EC2 server.

11. Background Process – PM2 (Optional) 🔄
PM2 can keep a Node.js process running in the background and help monitor or restart it. It is not listed as a dependency in the uploaded package.json, so install it separately only if needed.

Install PM2:
sudo npm install -g pm2
Start the application:
pm2 start app.js --name jenkins-node-app
Useful commands:
pm2 status
pm2 logs jenkins-node-app
pm2 restart jenkins-node-app
pm2 stop jenkins-node-app
pm2 save
Automatic startup after a server reboot requires configuring PM2 startup for the server's operating system.

12. Jenkins and GitHub Webhook (Optional) 🔧
The application message mentions Jenkins and a webhook, but the uploaded app.js and package.json do not themselves configure a Jenkins pipeline or a GitHub webhook.

To add CI/CD automation:
1. Configure a Jenkins job or Jenkinsfile.
2. Give Jenkins secure access to the GitHub repository.
3. Configure a GitHub webhook to notify a reachable Jenkins endpoint.
4. Add pipeline stages for checkout, dependency installation, testing, and deployment.
5. Configure deployment credentials and server-side commands securely.
6. If PM2 is used, add an appropriate restart step to the deployment process.

13. Testing Checklist ✅
- [ ] Node.js and npm are installed.
- [ ] npm install completes successfully.
- [ ] npm start starts the server.
- [ ] http://localhost:3000/ displays the expected message.
- [ ] The terminal shows the server startup message.
- [ ] Jenkins and webhook work, if separately configured.
- [ ] EC2 deployment and PM2 work, if separately configured.

14. Future Enhancements 🚀
- Add automated tests.
- Create a Jenkinsfile.
- Configure a GitHub webhook.
- Deploy to AWS EC2 through a Jenkins pipeline.
- Use PM2 for process management.
- Configure Nginx and HTTPS for a production-style deployment.
- Add application logging and monitoring.

15. Conclusion 🎉
This project demonstrates a basic Node.js and Express.js web application. It shows how to define a route, return a text response, and manage application startup using npm.

It can be extended into a DevOps learning project by separately configuring GitHub webhooks, Jenkins CI/CD, AWS EC2 deployment, and PM2 process management.
Repository: Nodejs-app

Project type: Node.js Web Application
Port: 3000
