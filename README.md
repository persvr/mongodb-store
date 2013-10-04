The mongodb-store is an NodeJS implementation of the object store interface for mongodb,
providing access to mongodb databases for [Persevere](http://persvr.org), any other consumer that uses
the object store interface (Dojo also uses this interface), and for direct interaction. This
store supports RQL for convenient web-based querying that matches well with MongoDB
querying capabilities.

MongoDB providesa powerful backend for Perstore because it is specifically designed for JSON-style
object storage. This store has good querying capabilites, supporting a large set of 
the RQL operators.

Setup
=====

mongodb-store can be installed with NPM via:

	npm install mongodb-store

If you are using this with Persevere, please see the Persevere [documentation](http://persvr.org/Documentation).

Using
======

You can create a Mongo store by instantiating it with the collection to use:

	store = require("mongodb-store").MongoDB({
		collection: collection
	});


The MongoDB store looks to the configuration settings for configuration information (from local.json or rc), using either the
database.url property or the database.host, database.name, and database.port properties.
For example, our local.json could configuration the database:

	"database": {
		"host": "localhost",
		"name": "wiki",
	},

(we omitted the port, which defaults to 27017)

We also must indicate which collection to use for the store. This is provided in the options
parameter to the constructor.

This store is only available for NodeJS.


Licensing
--------

mongodb-store is part of the Persevere project, and therefore is licensed under the
AFL or BSD license. The Persevere project is administered under the Dojo foundation,
and all contributions require a Dojo CLA.

Project Links
------------

See the main Persevere project for more information:

### Homepage:

* [http://persvr.org/](http://persvr.org/)