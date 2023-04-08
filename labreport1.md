# Lab Report 1: Remote Access and File System

### Overview
In Week 1, we learned how to log into a course-specific account on ieng6. In the following blog, I will be laying out the series of steps I took to access a remote server from my own computer. I will also be going over some newly learned commands that I used to navigate my own computer and the remote computer. Please note that the following instructions are specifically only for Mac users since I went through the entire process with a Macbook. If you use a Windows computer, the following steps may not work for you. 

### Step 1: Installing Visual Studio Code

Since I had already installed Visual Studio Code, often referred to as VSCode, I actually did not need to go through this step. If I did not have VSCode, I would have needed to download it. VS Code is a code editor developed by Microsoft, and it has consistently been one of the most popular integrated development environment (IDE) among developers. I have used a variety of IDEs, and I must say that VSCode is by far my favorite IDE. If you want to download VSCode, click [here](https://code.visualstudio.com/download). It is a very easy process! The picture below shows you the VSCode interface.
![VSCode-interface](vscodeinterface.png)

### Step 2: Remotely Connecting

I had so much difficulties connecting to a remote server. However, I don't think you will experience much difficulties. It is actually a very simple process that was unnecessarily hard for me because my course-specific account had some sort of bug. To connect to a remote server, all you need to do is follow the following steps: 
1. Lookup your course-specific username [here](https://sdacs.ucsd.edu/~icc/index.php)
2. If you do not know your password or need to reset your password, follow the instructions [here](https://drive.google.com/file/d/17IDZn8Qq7Q0RkYMxdiIR0o6HJ3B5YqSW/view)
3. Open a fresh new terminal in your VSCode
4. Type in the command `ssh cs15lsp23zz@ieng6.ucsd.edu` with zz replaced by the letters in your course-specific account. 
5. If you are trying to connect to a remore server for the first time, you may see a message similar to `The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established. RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec. Are you sure you want to continue connecting (yes/no/[fingerprint])? `. I typed in "yes" in the terminal to continue. 
6. You will be prompted for your password. Type in your password.
7. Pray that you get succesfully logged into the remote server after you type in your password. If successful, you should see a message like this `# Now on remote server
Last login: Sun Jan  2 14:03:05 2022 from 107-217-10-235.lightspeed.sndgca.sbcglobal.net
quota: No filesystem specified.
Hello cs15lsp23zz, you are currently logged into ieng6-203.ucsd.edu

You are using 0% CPU on this system

Cluster Status 
Hostname     Time    #Users  Load  Averages  
ieng6-201   23:25:01   0  0.08,  0.17,  0.11
ieng6-202   23:25:01   1  0.09,  0.15,  0.11
ieng6-203   23:25:01   1  0.08,  0.15,  0.11

Sun Jan 02, 2022 11:28pm - Prepping cs15lsp23`

### Step 3: Trying Some Commands
