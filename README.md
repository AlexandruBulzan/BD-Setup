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

# Step 2: Setting Up Your Git Account

To set up Git with your GitHub account, follow these steps to configure your user details and manage credentials:

1. **Configure User Information:**
   Set your GitHub username and email associated with your GitHub account using the following commands:
   ```bash
   git config --global user.name "your_username"
   git config --global user.email "your_email@example.com"
   ```
   Replace `your_username` with your actual GitHub username, and `your_email@example.com` with the email you use on GitHub.

2. **Credential Management:**
   To store your credentials for future use, enable the credential manager with the command below:
   ```bash
   git config --global credential.helper manager
   ```

3. **Authentication:**
   When you execute a Git command that requires authentication (such as `git push`), you will be prompted to enter your username and a Personal Access Token (PAT). You can generate a PAT quickly on GitHub if you don't already have one. Once entered, the credential manager will store these details for future Git commands.

This setup streamlines your workflow by remembering your login details on your machine, making your interactions with remote repositories more efficient.

# Step 3: Start developing your project

### 3.1 Creating a New Project Directory:

Follow these steps to create a new directory for your project and initialize it as a Git repository:

1. **Create a New Folder:**
   Open your terminal and navigate to the folder that you want. Then create a folder named `BD-Setup` and navigate into it using the following commands:
   ```bash
   cd Desktop
   mkdir BD-Setup
   cd BD-Setup
   ```

2. **Initialize a Git Repository:**
   Once you are inside your new directory, initialize it as a Git repository with the following command:
   ```bash
   git init
   ```
   This command creates a new `.git` directory in `BD-Setup`, which will track all changes made to the files in this directory and store the version history.

	<img width="566" alt="2" src="https://github.com/user-attachments/assets/657e13b3-34e0-4045-a5c8-1cc0db9e2da5">

### 3.2 Adding a `.gitignore` File

To prevent unnecessary files from being tracked by Git, you can create and configure a `.gitignore` file in your project directory:

1. **Create and Configure `.gitignore`**
   Open your terminal in your project directory and execute the following commands to create a `.gitignore` file and add `.DS_Store` (a common unwanted file in macOS) to it:
   ```bash
   echo ".DS_Store" >> .gitignore
   ```

2. **Add and Commit `.gitignore`**
   Add the `.gitignore` file to your staging area and commit it to your repository with these commands:
   ```bash
   git add .gitignore
   git commit -m "Added .gitignore to exclude unnecessary files"
   ```
   This step ensures that the files listed in `.gitignore` are ignored by Git, keeping your repository clean of any unnecessary files.

	<img width="802" alt="3" src="https://github.com/user-attachments/assets/b44b3d0d-4453-4924-a074-f530ca12ba11">


### 3.3. Link Local Repository to GitHub

Establish a connection between your local repository and GitHub to push your changes:

1. **Add Remote Repository**
   In your terminal, link your local repository to a remote GitHub repository using the following commands:
   ```bash
   git remote add origin https://github.com/AlexandruBulzan/BD-Setup.git
   ```

2. **Push Changes**
   Push your changes to the GitHub repository by setting the remote 'origin' and branch 'main' as default for future pushes:
   ```bash
   git push -u origin main
   ```

### 3.4. Add Project Setup Files

Prepare your project structure with essential scripts and directories:

1. **Create Scripts and Directories**
   Generate shell scripts for documentation and testing, and create the necessary folders for your project organization:
   ```bash
   touch generate-documentation.sh run-unit-tests-and-coverage.sh
   mkdir .devcontainer .vscode docs source src tests project_structure
   ```

2. **Commit and Push `generate-documentation.sh`**
   Add, commit, and push the documentation script to your repository:
   ```bash
   git add generate-documentation.sh
   git commit -m "Script to build project documentation"
   git push origin main
   ```

3. **Commit and Push `run-unit-tests-and-coverage.sh`**
   Add, commit, and push the unit test script which also generates an HTML coverage report:
   ```bash
   git add run-unit-tests-and-coverage.sh
   git commit -m "Script to execute unit tests and generate HTML coverage report"
   git push origin main
   ```

### 3.5. Set Up Development Container

Configure your development environment within a container:

1. **Navigate and Create Configuration Files**
   Change to the `.devcontainer` directory and create the necessary Docker configuration files:
   ```bash
   cd .devcontainer
   touch Dockerfile devcontainer.json
   ```

2. **Edit Dockerfile**
   Open the Dockerfile to edit and configure your container environment:
   ```bash
   nano Dockerfile
   ```


