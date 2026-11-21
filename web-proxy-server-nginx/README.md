NGINX Web Server, Reverse Proxy & Docker Application Scaling 

Overview

Deployment of a web application using NGINX, Node.js, Express, and Docker Compose.

The objective is to configure NGINX as the public-facing web entry point and reverse proxy, then containerize a Node.js application and deploy three independent instances behind NGINX.

NGINX distributes incoming HTTP requests across the three application instances using its default round-robin load-balancing method. 

=====================The "Application" highlights projects from CACooper.==============================
_______________________________________________________________________________________________________________ 

By completing this lab, you should be able to:

Install and configure NGINX on Ubuntu Server.
Understand the role of a web server and reverse proxy.
Understand how NGINX forwards requests to backend applications.
Install and configure Node.js and Express.
Build a Docker image using a Dockerfile.
Deploy multiple instances of one application.
Use Docker Compose to manage multiple containers.
Configure NGINX as a load balancer.
Implement container health checks.
Inspect Docker container status and application logs.
Troubleshoot application, networking, and reverse proxy issues.
Understand the difference between application redundancy and infrastructure high availability. 
_____________________________________________________________________________________________________________

LAB Architecture

  CLIENT--------------v
                      |
                      |
                HTTP Request
                      |
                      v
             NGINX WEB SERVER
             Reverse Proxy
             Load Balancer
                Port 8080
                      |
             Docker Network
                      |
          +-----------+-----------+
          |           |           |
          v           v           v
       APP 1        APP 2       APP 3
       Node.js      Node.js     Node.js
       Express      Express     Express
       :3000        :3000       :3000
          |           |           |
          +-----------+-----------+
                      |
                      v
                HTML Application
                 public/index.html 






