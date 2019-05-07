# Data Persistance

Data persistance is achieved via Data Gateways. Data Gateways are adapters 
that know how to store, retrieve and query data in a persistent data store of 
some sort.

Data Gateways are interchangeable for a given Story. The data persistence 
mechanism (database, queue or other storage product) is treated as a plugin
in RADiQL CA (Clean Architecture).