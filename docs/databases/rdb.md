A relational [[Databases (KB)|database]] is a type of database that stores and provides access to data points that are related to one another. Relational databases are based on the relational model, an intuitive, straightforward way of representing data in tables. 

In a relational database, each row in the table is a record with a unique ID called the key. The columns of the table hold attributes of the data, and each record usually has a value for each attribute, making it easy to establish the relationships among data points. 

When a user needs to access specific information, they can use a key to access all the tables of data that have been pre-determined to be related to that key.

Suppose you're working for a company that sells clothes online. Your organization uses a relational database to manage data related to shipping, customer information, inventory, and website traffic. You have a key to this database that accesses all tables related to shipping, and you need to find out if you have enough inventory to ship out last week's orders.

Since the relational database recognizes that there's a relationship between shipping information and inventory, you can use your key to access inventory numbers and shipping requests to compare data. 

During this request, you won't access any information about website traffic because your key only accesses the tables of data that are related to shipping.