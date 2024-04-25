UUIDv5 is a version of the universally unique identifier (UUID) that uses [[SHA-1]] hashing to generate a UUID from a namespace identifier and a name. It's specified in RFC 4122 and is designed to create deterministic and unique IDs.

UUIDv5 uses the SHA-1 hashing algorithm on a namespace and a specific name to generate the UUID. The namespace is another UUID that acts as a domain or category identifier, ensuring uniqueness across different namespaces. Unlike [[UUIDv4]] which is randomly generated, UUIDv5 is deterministic. The same namespace and name combination will always generate the same UUID.

Unlike [[UUIDv1]], UUIDv5 doesn't use the [[MAC address]] of the generating machine, thus avoiding the privacy issues associated with UUIDv1. The non-random, deterministic nature of UUIDv5 means it's predictable if the namespace and name are known. However, this predictability is by design and is not typically a vulnerability in the context of its intended use.

UUIDv5 is useful in scenarios where you need a consistent identifier generated from a specific name within a known namespace. For example, generating a consistent ID for a user based on their username. It can be used in web [[APIs]] to generate unique identifiers for resources.

Identifying a UUID as being of version 5 (UUIDv5) can be accomplished by examining its structure and specific components. Like other versions of UUIDs, UUIDv5 is a 128-bit number and is typically represented as a 36-character string (including hyphens) composed of hexadecimal digits. It's structured into five groups, represented as 8-4-4-4-12 characters.

1. **Version Digit**: The version of the UUID is indicated by the first character of the 13th hexadecimal digit. For UUIDv5, this digit will be `5`.
2. **SHA-1 Hashing**: UUIDv5 uses SHA-1 hashing of a namespace identifier and a name to generate the UUID. However, this hashing process is not evident from the UUID itself.
3. **Namespace**: UUIDv5 is generated from a namespace, but the namespace used is not directly identifiable from the UUID.

An example of a UUIDv5 string could look like this:

```bash
c6db45fb-8d5c-52b9-b7c0-1f6e8df6e5d6
```

The `5` at the start of the third group (`52b9`) indicates that this is a version 5 UUID.
