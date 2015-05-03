---
layout: page
title:  "Treehouse VM Installation Guide"
date:   2015-04-28 14:29:00
categories: mac
---
## What is the Treehouse VM?
The Treehouse Virtual Machine is a Vagrant controlled linux virtual machine. This VM is used in different Treehouse courses to facilitate the installation of Ruby on Rails and associated libraries and versions. Many of the VMs have the following installed:

* Ruby
* Ruby on Rails
* MySQL
* PostgreSQL
* Sqlite3
* Imagemagick
* curl

It is not necessary to use the VM to follow along with Ruby and Rails related Treehouse courses if you already have the libraries and prerequisites installed.

## Download and Install VirtualBox
VirtualBox is free virtualization software. Head on over to the following address and download the **latest** version of VirtualBox and the **VirtualBox Extension Pack** for your Linux distribution:

* [VirtualBox Downloads](https://www.virtualbox.org/wiki/Linux_Downloads)

Then proceed to install VirtualBox as you would any other software.

## Download and Install Vagrant
Vagrant is a piece of software used to control and install virtual machines. Download the latest version of Vagrant and install it as you would any other piece of software for your computer:

* [Vagrant Downloads](http://www.vagrantup.com/downloads.html)

Once you have finished this step, **please reboot your computer**.

## Download the Treehouse VM Files

The final download necessary is the Treehouse VM specific to the course you are taking. Head over to the following site:

* [Treehouse VM Downloads](http://vm.teamtreehouse.com/)

Select the course you are taking and download the appropriate virtual machine. This will contain only a zip file. Once you have the zip file, unzip it and follow along with the rest of this tutorial.


## Set up the Project
Find the zip file where you downloaded the Treehouse VM and extract it. Remember the folder or directory where it was extracted. In your terminal, type the following to get to that folder:

```
cd projects
```

Now we can launch vagrant. Type the following:

```
vagrant up
```

That starts the virtual machine. If this is the first time you are running that specific virtual machine, it will need to be downloaded and configured.

Once the virtual machine has downloaded, type the following:

```
vagrant ssh
```

That will put you inside of the virtual machine and you can proceed to follow along with the course. Great work!

If you get any errors about shared folders, type the following:

```
vagrant plugin install vagrant-vbguest
```

Then **reboot your computer** and attempt the `vagrant up` section above again.

To stop the virtual machine type the following:

```
vagrant halt
```

## Setting up a Rails Application
If you’re following a Rails related course, such as _Build a Rails API_, you need to follow just a few more steps to get everthing set up. Go back to your terminal and type the following:

```
cd odot
bundle
bin/rake db:create:all
touch config/secrets.yml
```

The last command creates a file called `secrets.yml` in the config directory. We need to fill that out. Open that up in a text editor ([Sublime Text](http://sublimetext.com) is a popular choice) and type the following:

```
development:
  secret_key_base:
```

Now we have to generate a secret! Go back to the terminal application and type the following:

```
bin/rake secret
```

That will spit out a long stream of letters and numbers. Paste the results after the `secret_key_base: ` and save the file.

Go back to your terminal and type the following:

```
bin/rake db:migrate
```

Done!

## Getting Help
By following the steps above, you should now have the Treehouse VM installed. If you are having trouble, post in the [Treehouse Forum](http://teamtreehouse.com/forum) with as many details as possible.
