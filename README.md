## INTRODUCTION

The **MERN stack** (MongoDB, Express, React, and Node.js) is a popular technology stack used to build robust, full-stack JavaScript web applications. This study guide will walk you through setting up a basic project using the MERN stack, covering installation, environment configuration, and key components of a to-do app. The project highlights essential skills for developing, testing, and deploying web applications using the stack.

## Prerequisites

Before we proceed, ensure you have the following software installed:

- **MongoDB**: This is a No SQL database that offers flexible, document-based storage.

- **Express.js**: This framework that helps Node.js to communicate, it helps in simplifying the creation of robust APIs and web applications.

- **React.js**: This is the framework that holds the front-end together, and in place. Here, we can paint interactive user interfaces with the great efficiency.

- **Node.js**: This one is the backstage software that helps in orchestrating server-side JavaScript execution efficiently.

## Step 0: Setting the environment for development

Before we go into the code, let's set up our development environment.

1. **Launching the EC2 Instance**: We're going for the t3.small instance running Ubuntu 24.04 LTS (HVM) in the us-east-2 region. 

2. **SSH Key**: We've attached our ssh-key to access the instance - whilst creating the instance. This helps us to access the instance securely without the need for a password.

3. **Security Group Configuration**: When we are creating the instance, we set up a digital bouncer (the security group) to allow the right traffic in:

- Port 80 (HTTP): The front door for web traffic.

- Port 22 (SSH): Our backdoor for maintenance.

- Ports 5000 and 3000: These ports were not enabled at first, but later during the course of deploying the app, was opened.

![project](/images/mern.jpg)

![project2](/images/mern2.jpg)

4. **Connecting to the Instance**: To connect to the instance, I implemented the Terminal windows app for this and I ran:

```bash
ssh -i "ssh-key.pem" ubuntu@<instance:IP>
```

