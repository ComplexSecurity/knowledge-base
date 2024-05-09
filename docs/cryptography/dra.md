The Double Ratchet Algorithm is a key management algorithm designed to provide secure end-to-end encryption for instant messaging applications. It was developed as part of the [Signal Protocol](../protocols/signal.md) by Open Whisper Systems, and it's used in popular messaging apps like Signal, WhatsApp, and Facebook Messenger. The algorithm is named for its dual mechanisms, or "ratchets," which are used to update the keys for each message.

The algorithm frequently changes encryption keys, using a new key for every message. This practice, known as "ratcheting," ensures that even if a key is compromised, only a small part of the conversation can be decrypted. Because it constantly updates keys, the algorithm provides forward secrecy. If a key is compromised, past messages remain secure since they were encrypted with different keys.

The Double Ratchet Algorithm is designed to work in environments where both parties are not always online at the same time, typical in modern messaging applications.

The Double Ratchet Algorithm combines a [Diffie-Hellman](../cryptography/dh.md) key exchange with a symmetric-key ratchet to update the keys for each message:

1. **Diffie-Hellman Ratchet**: Used intermittently to provide new key material. When two parties exchange messages, they also periodically send new Diffie-Hellman public keys. Each party combines the other's public key with their own private key to derive new shared secrets.
2. **Symmetric-Key Ratchet**: Also known as the "KDF-chain" (Key Derivation Function chain), this ratchet is used for every message. It takes the output of the Diffie-Hellman ratchet and derives new keys for each message, ensuring that each message has a unique encryption key.

In a messaging app, when a user sends a message:

1. The app uses the Double Ratchet Algorithm to generate a new message key.
2. The message is encrypted with this key.
3. The receiver uses the same algorithm to generate the corresponding key to decrypt the message.

A conceptual example:

```python
# Pseudo-code example
# Assuming Alice and Bob have already established shared secrets
alice_ratchet = DoubleRatchet(alice_shared_secret)
bob_ratchet = DoubleRatchet(bob_shared_secret)

# Alice sends a message
alice_key = alice_ratchet.next_key()
encrypted_message = encrypt(alice_key, "Hello, Bob!")

# Bob receives and decrypts the message
bob_key = bob_ratchet.next_key()
decrypted_message = decrypt(bob_key, encrypted_message)
```
