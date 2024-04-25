UUIDv1 is a version of the universally unique identifier (UUID) specified in RFC 4122. It is generated using a combination of the host computer's [[MAC address]] and the current timestamp. UUIDv1 uses the current time (down to 100-nanosecond intervals) since a specific epoch (15 October 1582) as part of the UUID. This ensures that UUIDs generated at different times are unique.

The UUID includes the MAC address of the host computer's network card, which helps ensure uniqueness across different devices. Like other UUIDs, it is a 128-bit value formatted as a string of hexadecimal digits, typically displayed in 5 groups separated by hyphens.

Since UUIDv1 contains the MAC address of the machine where it was generated, there is a potential privacy issue. The MAC address can be used to identify the machine or, in some cases, even track its location. The use of a timestamp makes UUIDv1 somewhat predictable, which might be a concern in certain applications where unpredictability is crucial (such as in cryptographic applications).

UUIDv1 can be used in web applications as unique identifiers for objects, transactions, or records. It is particularly useful in distributed systems where coordination between different parts of the system to generate unique IDs is challenging. They are often used as primary keys in database tables. The time-based nature of UUIDv1 can offer better performance for insert operations in certain database systems compared to the random nature of [[UUIDv4]].

They can also be used for generating unique session IDs in web applications.

Given the privacy and predictability concerns with UUIDv1, many applications opt for [[UUIDv4]], which is randomly generated, or [[UUIDv5]], which uses [[SHA-1]] hashing. These versions do not disclose hardware-related information and offer less predictability.

Identifying a UUID as being of version 1 (UUIDv1) can be done by examining its structure and specific components. A UUID is a 36-character string (including hyphens) composed of hexadecimal digits. It's structured into five groups, typically represented as 8-4-4-4-12 characters. The version and variant of a UUID are encoded in specific positions within the string.

1. **Version Digit**: The version of the UUID is indicated by the first character of the 13th hexadecimal digit. For UUIDv1, this digit will be `1`.
2. **Timestamp**: UUIDv1 is generated based on the current timestamp (time since 15 October 1582 in 100-nanosecond intervals). This timestamp forms the first part of the UUID.
3. **MAC Address**: The last 12 hexadecimal digits of UUIDv1 represent the MAC address of the machine where it was generated.

An example is:

```bash
6ba7b810-9dad-11d1-80b4-00c04fd430c8
```

- The `1` at the start of the third group (`11d1`) indicates that this is a version 1 UUID.
- The `d` in `11d1` (specifically the most significant bits of this hexadecimal digit) indicates the UUID variant; in standard UUIDs, this is typically `8`, `9`, `a`, or `b`.
