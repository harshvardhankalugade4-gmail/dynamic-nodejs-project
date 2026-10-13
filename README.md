# Node.js Application Deployment on AWS EC2

## 1. Introduction

This project demonstrates how to deploy and run a Node.js application on an Amazon Web Services (AWS) EC2 instance.

The application is hosted on a cloud server and accessed through a web browser using the EC2 instance's public IP address and port 3000.

PM2 is used to start and manage the Node.js application process.

## 2. Project Objectives

- Deploy a Node.js application on AWS EC2.
- Understand basic Linux server management.
- Run and manage the application using PM2.
- Configure EC2 security group inbound rules.
- Access the application through a public IP address.
- Verify the application status and output.

## 3. Technologies Used

- **AWS EC2:** Cloud server used to host the application.
- **Node.js:** JavaScript runtime for running the application.
- **PM2:** Process manager for managing the application.
- **Linux:** Operating system environment.
- **SSH:** Used to connect to the EC2 instance.
- **GitHub:** Used to store the source code and project documentation.

## 4. Project Architecture

The user accesses the application through a web browser using the EC2 public IP address and port 3000.

The EC2 security group allows the required network traffic to reach the server. The Node.js application processes the request and returns a response to the browser.

PM2 manages the Node.js application process.

## 5. AWS EC2 Instance

An EC2 instance provides the cloud environment required to run the Node.js application.

The instance must be running and configured correctly to host the application.

**Screenshot:** AWS EC2 Instances page showing the running instance.

## 6. Security Group Configuration

The EC2 security group controls incoming network traffic to the instance.

The following inbound rules are relevant to this project:

| Type | Port | Purpose |
|---|---|---|
| SSH | 22 | Remote server access |
| Custom TCP | 3000 | Access to the Node.js application |

SSH access should be restricted to trusted IP addresses. Application ports should only be exposed to the sources that require access.

**Screenshot:** EC2 Security Group inbound rules.

## 7. Application Deployment Using PM2

PM2 is used to start and manage the Node.js application.

Start the application:

```bash
sudo pm2 start app.js
