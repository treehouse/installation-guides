---
layout: page
title:  "Installing Homebrew on Mac"
date:   2016-05-14 13:31:00
categories: mac
---

## Installation
Homebrew is package manager for Macs which makes installing lots of different software like Git, Ruby, and Node simpler. Homebrew lets you avoid possible security problems associated with using the `sudo` command to install software like Node.

## Prerequisites
* **You should have some familiarity with the Mac Terminal application** since you'll need to use it to install Homebrew. The Terminal application is located in the Utilities folder in the Applications folder.
* **Dependencies.** You need to install one other piece of software before you can install Homebew:
  * **Xcode.** Install Apple's Xcode development software: [Xcode in the Apple App Store](http://itunes.apple.com/us/app/xcode/id497799835?ls=1&mt=12). 

## Installation Overview
Installing Homebrew is straightforward as long as you understand the Mac Terminal. The Homebrew installation process guides through each step.

## Installation Steps
* **Open the Terminal app**.
* **Type** `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` You'll see messages in the Terminal explaining what you need to do to complete the installation process. You can learn more about Homebrew at the [Homebrew website](http://brew.sh/).

## How to Update Homebrew
New versions of Homebrew come out frequently, so make sure you update it before updating any of the other software components that you've installed using Homebrew.
* In Terminal type `brew update`

## How to Uninstall Homebrew
* **Open the Terminal app**
* **Type** `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/uninstall)"` This downloads and runs the uninstaller script. Follow the instructions and Homebrew will be removed from your computer.
