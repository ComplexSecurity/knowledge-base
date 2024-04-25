X3DH, which stands for Extended Triple [[Diffie-Hellman]], is a key agreement protocol designed to establish a shared secret between two parties. It's part of the [[Signal Protocol]], developed by Open Whisper Systems and used in encrypted messaging services like Signal, WhatsApp, and Facebook Messenger.

X3DH is specifically designed to facilitate secure and private communication in an asynchronous environment, such as modern messaging systems where both parties might not be online simultaneously.

X3DH works by combining public key cryptography with the Diffie-Hellman key exchange principle to establish a shared secret that can then be used to encrypt messages. The protocol involves several keys to ensure security, even if some of them become compromised. The key components include:

1. **Identity Keys**: These are long-term public-private key pairs that are used to verify the identity of each user.
2. **Signed Prekey**: A long-term public-private key pair, where the public key is signed by the user's identity key. It provides a fallback for cases where one-time prekeys are not available.
3. **One-time Prekeys**: These are pre-generated one-time-use key pairs that add an additional layer of security. They are used only once and then discarded.
4. **Ephemeral Keys**: These are temporary public-private key pairs generated for each new key exchange process.

When a user wants to initiate a conversation, they retrieve the recipient's identity key, signed prekey, and one of the one-time prekeys from the server. The sender combines their ephemeral key with the recipient's keys (identity key, signed prekey, and one-time prekey) using the Diffie-Hellman process to generate shared secret components. The shared secret components are then combined (typically concatenated and then hashed) to form a master secret. This master secret is further used to derive encryption keys for secure communication.

Even if long-term keys are compromised, past session keys cannot be retroactively decrypted, as each session has its unique set of keys. X3DH is designed to work in scenarios where both parties are not necessarily online at the same time, which is common in messaging applications. By using a combination of long-term and ephemeral keys, X3DH is robust against various types of cryptographic attacks, even if some keys are compromised.

X3DH is an integral part of the Signal Protocol and is used in various encrypted messaging applications. Its role is to securely establish the keys necessary for encrypting messages, ensuring that the content of the communication remains private and secure.
