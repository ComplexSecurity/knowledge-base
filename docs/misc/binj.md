Binary JSON (BJSON) is a concept that typically refers to BSON, which stands for "Binary JSON." BSON is a binary-encoded serialization of [[JavaScript Object Notation|JSON]]-like documents. It is designed to be more efficient in terms of space and speed when compared to JSON, especially in the context of certain types of data. 

BSON is used in several [[Non-relational Database|NoSQL]] databases, most notably [[MongoDB]].

BSON's binary format allows for more efficient storage and faster access to data. This is particularly beneficial when working with large datasets or in environments where performance is critical.

Unlike JSON, which primarily supports text, BSON supports a wider range of data types, including int, long, date, floating point, and decimal128. It also supports more complex types like byte arrays, making it suitable for storing binary data.

BSON is essentially a binary representation of JSON data. It extends the JSON model to provide additional data types and to be efficient for encoding and decoding within different languages.

BSON is widely used in NoSQL databases like MongoDB. In these databases, BSON allows for the storing and querying of documents in a way that is more space-efficient and faster than if the documents were stored in plain JSON format.

