A CRUD API is an interface that allows software applications to interact with a database using four basic operations: **Create**, **Read**, **Update**, and Delete**.** These operations form the acronym CRUD.

Each part is as follows:

- Create - allows new data to be added to the database
- Read - used to retrieve data from the database
- Update - modifies existing data in the database
- Delete - removes data from the database.

In the context of an API, they are typically executed over the Internet. The API serves as a middleman between a client and a server where the database is hosted. It uses [[HTTP Methods]] to perform these operations such as:

- Create - associated with POST
- Read - associated with GET
- Update - associated with PUT or PATCH
- Delete - associated with DELETE method

However, in more modern web apps, the update and delete operations do not use PUT/DELETE but instead use POST to specific endpoints such as POST /posts/1 or POST /posts/1/delete.
