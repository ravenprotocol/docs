# RavCom

RavCom is a common library that contains various methods to interact with the databases like MySQL, Redis, PostgreSQL, and others. It is a common library used in most of our libraries.

[Github](https://github.com/ravenprotocol/ravcom.git)

## Prequisites

#### MySQL Server

**Linux**
```
sudo apt-get update
sudo apt-get install python3-dev default-libmysqlclient-dev build-essential
sudo apt-get install mysql-server
sudo apt-get install mysql-client
```

**Mac**

1. Install [homebrew](https://docs.brew.sh/Installation)

2. Install and start MySQL
```
brew update
brew install mysql
brew tap homebrew/services
brew services start mysql
```

3. Run CLI wizard to create a root user
```
mysql_secure_installation
```


#### Redis DB
**Linux**

TBD

**Mac**
```
brew update
brew install redis
brew services start redis
```

#### Create MySQL Tables
**Linux**

TBD

**Mac**

1. Login to mysql

        mysql -u root -p your_root_password

2. Create RDF db

        > CREATE DATABASE rdf;

3. Run one-liner to create tables

        RDF_MYSQL_PASSWORD=your_root_password python3 -c "from ravcom import reset; ravcom.reset();"

*TODO: Add to setup.py as a script*
*TODO: Add .env file for passwords*

## Installation

Create a virtual environment
    
    virtualenv ravcom -p python3
    
Activate the virtual environment
    
    source ravcom/bin/activate
    
Install ravcom

    python3 setup.py install
    
## Usage

Import ravcom

    from ravcom import ravcom
    
Reset everything 

    from ravcom import reset
    reset()
    
Delete and create database

    from ravcom import delete_create_database
    delete_create_database()

Database Manager can be accessed using

    from ravcom import ravdb
    
Create op

    op = ravdb.create_op(**kwargs)
    
Get op

    op = ravdb.get_op(id=1)
    
Get op by name

    op = ravdb.get_ops_by_name(op_name="x", graph_id=1)
    // Here graph id is optional
    
Get op status

    ravdb.get_op_status()

Create graph

    graph = ravdb.create_graph()

Get graph

    graph = ravdb.get_graph(graph_id=1)
    
Get graph ops

    graph = ravdb.get_graph_ops(graph_id=1)

Create client

    client = ravdb.create_client(**kwargs)
    
Get client

    client = ravdb.get_client(client_id=1)
    
Get all ops

    ops = ravdb.get_all_ops()
    
Get all graphs

    graphs = ravdb.get_all_graphs()
    
Get all clients

    clients = ravdb.get_all_clients()
    
