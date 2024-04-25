UUIDv4 refers to a version 4 universally unique identifier (UUID), which is a type of UUID that is randomly generated. A UUID is a 128-bit number used to uniquely identify information in computer systems. The "v4" indicates that it's version 4, which is one of the several versions of UUIDs specified in RFC 4122.

UUIDv4 is generated using random or pseudo-random numbers. The randomness feature ensures a very low probability of generating duplicate UUIDs. A UUIDv4 is composed of hexadecimal digits, displayed in 5 groups separated by hyphens, in a form such as **550e8400-e29b-41d4-a716-446655440000**. The total number of characters is 36 (32 hexadecimal characters and 4 hyphens).

In UUIDv4, the version number (4) is set in the 13th character, and the variant is set in the 17th character. The variant bits indicate the UUID layout; for UUIDv4, this is usually `8`, `9`, `A`, or `B`.

The primary usage of UUIDv4 is when you need a unique identifier that you can generate without needing to coordinate with a central authority. This makes UUIDv4 ideal for distributed systems. UUIDv4 is often used as a unique key in databases, ensuring that each record can be uniquely identified across different tables, databases, or even different systems.

UUIDv4 is used in software development for various purposes, such as transaction IDs, unique session identifiers, and any other scenario where a unique identifier is required.

Due to its random nature, UUIDv4 has a very low probability of duplication, even when generated across different machines independently. UUIDv4 can be generated without needing a central authority to avoid duplicates, making it suitable for decentralized applications.

Unlike [[UUIDv1]], which is time-based and sequential, UUIDv4 is random, offering better privacy (no embedded timestamps or [[MAC Address|MAC addresses]]). In database systems, the use of UUIDv4 as primary keys may have implications for storage and performance, as they are larger and not sequential compared to traditional integer IDs.
