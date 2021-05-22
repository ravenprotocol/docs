# Raven Distribution Framework (Alpha)

The Raven Distribution Framework (RDF) is a community-developed implementation of the decentralized computing model outlined by [Raven Protocol](https://www.ravenprotocol.com/). Within the Raven ecosystem today, there are two main actors: 

* **Users:** Create models that need to be trained
* **Clients:** Provide computational power to train the models

For Users, there are three core libraries that drive the main function for computation distribution ([RavCom](ravcom.md), [RavOP](ravop.md), and [RavSock](ravsock.md)), along with a growing list of libraries that extend the core to be more developer-friendly to use.

For Clients, there is a frontend Javascript library (RavJS) that enables anyone with a browser to contribute processing power. Additional clients are in consideration, such as Go and Rust (looking for community devs!).

### Core libraries

* [RavCom](ravcom.md): Handles operation distribution and communication with databases.
* [RavOP](ravop.md): Core operations models for distributed computation
* [RavSock](ravsock.md): Socket server for client connections

### Helper libraries
* [RavML](ravml.md): Machine learning specific library
* RavDL (Coming soon): Deep learning specific library
* [RavViz](ravviz.md): Frontend dashboard to see operations and client connections

### Client libraries
* [RavJS](ravjs.md): Frontend script for browers to retrieve and calculate operations from Users