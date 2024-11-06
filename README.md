# BD-Setup

This document contains the setup for the BD-Setup project, including configuration for Git, Docker, and the development environment. Follow the instructions below to set up everything properly.

# Step 1: Prerequisites
	1.	Install Git: Download and install it from git-scm.com
	2.	Install Docker: Download and install it from docker.com
 	3. 	Install VS code: very robust code editor - code.visualstudio.com along with VSCode Extension for Remote Containers

To make the connection between the project developed in Visual Studio and docker you need to install from the extension manager the extension called DEV CONTAINERS:

<img width="1448" alt="Screenshot 2024-11-05 at 23 53 31" src="https://github.com/user-attachments/assets/18872690-c686-487a-ac1f-5d94c7f9a304">


Ensure you have Git and Docker installed on your system:

<img width="565" alt="1" src="https://github.com/user-attachments/assets/babe8e97-40de-470a-aa63-01bc646989cc">


Make sure you install Docker Desktop for setting up and managing containers easily:

<img width="1336" alt="Screenshot 2024-11-05 at 23 39 49" src="https://github.com/user-attachments/assets/016d3402-8da0-435f-8d67-be4429ffc6d4">

# Step 2: Prerequisites

Here's a rephrased version of the Git configuration instructions suitable for a `readme.md` file:

---

### Setting Up Your Git Account

To set up Git with your GitHub account, follow these steps to configure your user details and manage credentials:

1. **Configure User Information**
   Set your GitHub username and email associated with your GitHub account using the following commands:
   ```bash
   git config --global user.name "your_username"
   git config --global user.email "your_email@example.com"
   ```
   Replace `your_username` with your actual GitHub username, and `your_email@example.com` with the email you use on GitHub.

2. **Credential Management**
   To store your credentials for future use, enable the credential manager with the command below:
   ```bash
   git config --global credential.helper manager
   ```

3. **Authentication**
   When you execute a Git command that requires authentication (such as `git push`), you will be prompted to enter your username and a Personal Access Token (PAT). You can generate a PAT quickly on GitHub if you don't already have one. Once entered, the credential manager will store these details for future Git commands.

This setup streamlines your workflow by remembering your login details on your machine, making your interactions with remote repositories more efficient.

---
