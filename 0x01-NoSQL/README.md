# 0x01. NoSQL Project

## Overview
This project focuses on **NoSQL** databases, with a deep dive into **MongoDB**. The aim is to introduce you to NoSQL concepts, showcase the differences between SQL and NoSQL, and teach you how to perform CRUD operations in MongoDB using **Python** and **PyMongo**.

### Timeline
- **Project Start:** October 21, 2024, 6:00 AM
- **Project End:** October 23, 2024, 6:00 AM
- **Checker Release:** October 21, 2024, 6:00 PM
- **Auto Review Launch:** At the deadline

## Resources
Here are essential resources to guide you through the project:
- [NoSQL Databases Explained](#)
- [What is NoSQL?](#)
- [MongoDB with Python Crash Course](#)
- [MongoDB Tutorial: Insert, Update, Remove, Query](#)
- [Aggregation in MongoDB](#)
- [Introduction to MongoDB and Python](#)
- [mongo Shell Methods](#)
- [Mongosh](#)

## Learning Objectives
By the end of this project, you should be able to explain:
- What NoSQL means and the differences between SQL and NoSQL.
- What ACID is and how it relates to database transactions.
- The concept of document storage.
- The types and benefits of NoSQL databases.
- How to query, insert, update, and delete data in a NoSQL database (MongoDB).
- How to use the MongoDB shell and Python to interact with MongoDB.

## Requirements
### MongoDB Command Files
- Files will be interpreted/compiled on **Ubuntu 18.04 LTS** using **MongoDB version 4.2**.
- All files should end with a new line.
- The first line of all files should be a comment: `// my comment`.
- A `README.md` file at the root of the project folder is mandatory.
- The length of files will be tested using `wc`.

### Python Scripts
- Python files will be interpreted/compiled using **python3 (version 3.7)** and **PyMongo (version 3.10)**.
- All files should end with a new line.
- The first line of all Python files must be `#!/usr/bin/env python3`.
- Use **pycodestyle** (version 2.5.*) for code styling.
- All modules and functions should have proper documentation.
- Your code should not be executed when imported (use `if __name__ == "__main__":`).

## Setup Instructions
To set up MongoDB on **Ubuntu 18.04 LTS**, follow these steps:

```bash
# Add MongoDB 4.2 repository
$ wget -qO - https://www.mongodb.org/static/pgp/server-4.2.asc | sudo apt-key add -
$ echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.2.list
$ sudo apt-get update

# Install MongoDB
$ sudo apt-get install -y mongodb-org

# Start MongoDB
$ sudo service mongod start

# Check MongoDB version
$ mongo --version
```

To install **PyMongo**, use:

```bash
$ pip3 install pymongo
```

Verify the installation:

```python
>>> import pymongo
>>> pymongo.__version__
'3.10.1'
```

## Troubleshooting
- If documents are not being created or if you encounter the error: `Data directory /data/db not found`, create the required directory:
  
```bash
$ sudo mkdir -p /data/db
```

- If `/etc/init.d/mongod` is missing, refer to an example file for configuration or use container-based setups.

## Using MongoDB in Containers
You can use a container running **Ubuntu 18.04** with MongoDB installed. To start MongoDB in a container:

```bash
$ service mongod start
```

## Example Commands
To list all databases:

```bash
$ cat 0-list_databases | mongo
```

Output will show the databases:

```bash
MongoDB shell version v4.2.8
connecting to: mongodb://127.0.0.1:27017
admin   0.000GB
config  0.000GB
local   0.000GB
```

## Conclusion
This project will enhance your knowledge of **NoSQL** databases and MongoDB. You will learn how to manage and query data in MongoDB using both the shell and Python, making you proficient in handling NoSQL databases.

Happy coding!

## Author
This project is developed and maintained by **BennyOnye**.