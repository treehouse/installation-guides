---
layout: page
title:  "Installing MongoDB on Windows"
date:   2015-12-28 12:00:00
categories: mac
---
## What's MongoDB?
MongoDB is a document database which belongs to a family of databases called NoSQL - not only SQL.  In MongoDB, records are documents which behave a lot like JSON objects in JavaScript.  Values in documents can be looked up by their field's key.  Documents can have some fields/keys and not others, which makes Mongo extremely flexible.  

This is different than SQL databases like MySQL and PostgreSQL, where fields correspond to columns in a table and individual records correspond to rows.

## Prerequisites
You should have a general familiarity with the Windows command prompt.

## Installing and Running MongoDB on a Windows Machine
* **Download the MongoDB installer file** from the [downloads section](https://www.mongodb.org/downloads#production) of the MongoDB website.
* **Find the dowloaded .msi file in the Windows Explorer.**  Double click the file and follow the prompts to install Mongo.  Unless you specify a customer directory **Mongo is installed in the `C:\mongodb` directory**.
* **Create the directory where MongoDB will store it's files.**  From the command prompt run `md \data\db`.  This is the default location.  However, other locations can be specified using the `--dbpath` parameter.  See [the Mongo docs](https://docs.mongodb.org/v3.0/tutorial/install-mongodb-on-windows/#set-up-the-mongodb-environment) for more information.
* **Start the mongodb daemon** by running `C:\mongodb\bin\mongod.exe` in the Command Prompt.
* **Connect to MongoDB using the Mongo shell** While the MongoDB daemon is running, from a different Command prompt window run `C:\mongodb\bin\mongod.exe`
