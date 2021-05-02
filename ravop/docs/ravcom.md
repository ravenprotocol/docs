# RavCom

RavCom is a common library that contains various methods to interact with the databases like MySQL, Redis, PostgreSQL, and others. It is a common library used in most of our libraries.

[Github](https://github.com/ravenprotocol/ravcom.git)

## Installation

Create a virtual environment
    
    virtualenv ravcom -p python3
    
Activate the virtual environment
    
    source ravcom/bin/activate

### Prequisites

#### MySQL Server

Linux
```
sudo apt-get update
sudo apt-get install python3-dev default-libmysqlclient-dev build-essential
sudo apt-get install mysql-server
sudo apt-get install mysql-client
```


Install Dependencies

    pip install git+https://github.com/ravenprotocol/ravcom.git
    
Install RavCom

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

    from ravcom import ravcom
    
Create op

    op = ravcom.create_op(**kwargs)
    
Get op

    op = ravcom.get_op(id=1)
    
Get op by name

    op = ravcom.get_ops_by_name(op_name="x", graph_id=1)
    Here graph id is optional
    
Get op status

    ravcom.get_op_status()

Create graph

    graph = ravcom.create_graph()

Get graph

    graph = ravcom.get_graph(graph_id=1)
    
Get graph ops

    graph = ravcom.get_graph_ops(graph_id=1)

Create client

    client = ravcom.create_client(**kwargs)
    
Get client

    client = ravcom.get_client(client_id=1)
    
Get all ops

    ops = ravcom.get_all_ops()
    
Get all graphs

    graphs = ravcom.get_all_graphs()
    
Get all clients

    clients = ravcom.get_all_clients()
    
