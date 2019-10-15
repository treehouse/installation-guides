---
layout: page
title:  "Installing Node.js® and NPM on Windows"
date:   2019-10-15 14:29:00
categories: windows
---
## What's Node.js®  and NPM?
Node.js® is a JavaScript-based environment which you can use to create web-servers and networked applications. You can also use it to perform helpful tasks on your computer such as concatenating and minifying JavaScript files and compiling Sass files into CSS.

NPM is a "package manager" that makes installing Node "packages" fast and easy. A package is just a code library that extends Node by adding useful features. For example, the "request" package simplifies the process of making HTTP requests so you can easily get web resources from other sites.

NPM is installed when you install Node.js®

## Prerequisites
* **You should have some familiarity with an application that lets you issue command line instructions.** For example, the Windows Command Prompt, PowerShell, [Windows Terminal](https://github.com/microsoft/terminal), or [Ubuntu terminal](https://tutorials.ubuntu.com/tutorial/command-line-for-beginners#0). 

## Installation Overview
Because most Node.js® and NPM projects are written for Linux tools and deployed on Linux servers, it is recommended to install Node.js on the Windows Subsystem for Linux (version 2, as it has signficant performance improvements for Node.js over WSL 1). 

Installing Node.js and NPM directly on Windows is still possible, but only recommended if just want to learn the very basic functions or plan to deploy your app to Windows Servers (which is fairly uncommon).

## Installation Steps

1. [Install the most recent version of Windows 10](https://www.microsoft.com/software-download/windows10).
2. Go to [Start > Settings > Windows Insider Program](ms-settings:windowsinsider), inside the Windows Insider Program window, select **Get started**, then Link an account.
3. [Register as a Windows Insider](https://insider.windows.com/getting-started/#register). If you aren't registered with the Insider program, you'll need to do so with your [Microsoft account](https://account.microsoft.com/account).
4. Choose to receive **Fast Ring updates**, confirm and choose to **Restart later**. 
5. From your **Start** menu, search for **Turn Windows features on or off**.
6. Scroll to find **Virtual Machine Platform** and **Windows Subsystem for Linux**, ensure that the box is checked to enable both, then select OK. **Restart your computer** when prompted.
7. Install [Ubuntu 18.04 LTS from the Microsoft Store](https://www.microsoft.com/store/productId/9N9TNGVNDL3Q). (This is a fairly large download and may take some time to install.)
8. Once downloaded, open the Ubuntu 18.04 command line. You will be asked to create an account name and password when you run it for the first time. 
9. Update Ubuntu by entering the command: `sudo apt update && sudo apt upgrade`
10. Open PowerShell (from your **Start** menu) and enter the command: `wsl -l` to view the list of WSL distributions that you have installed on your machine. You should now see Ubuntu-18.04 in this list.
11. Enter the command: `wsl --set-version Ubuntu-18.04 2` to set your Ubuntu installation to use WSL 2.
12. Verify the version of WSL each of your installed distributions are using with: `wsl --list --verbose`
13. Open your Ubuntu 18.04 command line.
14. Install cURL (a tool used for downloading content from the internet in the command-line) with: `sudo apt-get install curl`
15. New versions of Node and NPM come out frequently. For this reason, it is recommended to install Node Version Manager (nvm), with: `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash`
16. List which versions of Node are currently installed (should be none at this point): `nvm ls`
17. Install the latest stable (LTS) release of Node.js: `nvm install --lts`
18. You can install other releases/versions of Node.js this way as well, like the current release, `nvm install node`, but it is recommended to use the LTS release for most projects.
19. List what versions of Node are installed: `nvm ls`

## Test it!
Make sure you have Node and NPM installed by running simple commands to see what version of each is installed:

* **Test Node.** To see if Node is installed, open the Ubuntu command line tool, and type `node -v`. This should print the version number so you'll see something like this `v0.10.35`.
* **Test NPM.** To see if NPM is installed, type `npm -v` in the terminal. This should print the version number so you'll see something like this `1.4.28`
* **Create a test file and run it.** A simple way to test that node.js works is to create a simple JavaScript file. In your Ubuntu terminal, enter: `touch hello.js`, open this file with the built-in Nano editor: `nano hello.js`, and add the code `console.log('Node is installed!');`. Then **Ctrl+S** and **Ctrl+X** to save and exit Nano.
* To run the code simply open your command line program, navigate to the folder where you save the file and type `node hello.js`. This will start Node.js and run the code in the `hello.js` file. You should see the output `Node is installed!`.

![](imgs/node-win-verify.png)


## Running a local server with VS Code
The free [Visual Studio Code](https://code.visualstudio.com/download) text editor offers the [Remote-WSL Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl). With this extension, you can run VS Code on Windows and a Node.js server from your Linux subsystem to run your app. To learn more, visit [Developing in WSL](https://code.visualstudio.com/docs/remote/wsl) or check out the [Get started with Node.js on Windows](https://docs.microsoft.com/windows/nodejs/) docs.
