ROT13 ("rotate by 13 places") is a simple letter substitution cipher that replaces a letter with the 13th letter after it in the alphabet. ROT13 is a special case of the Caesar cipher which was developed in ancient Rome.

Each letter in the plaintext is replaced by a letter located 13 positions down the alphabet. Because the alphabet has 26 letters, ROT13 is its own inverse. Applying ROT13 to encrypted text decodes it, and applying it again re-encrypts it. For example, "hello" becomes "uryyb" under ROT13.

Websites sometimes use ROT13 to encode email addresses in [HTML](../web/html.md) source code, intending to prevent them from being easily harvested by spambots. While this can reduce the amount of spam, many sophisticated bots can easily decode ROT13.

In some programming contexts, ROT13 might be used to [obfuscate](../security/obfuscation.md) strings within the code. This can serve to lightly conceal messages, URLs, or other data within the source code from immediate recognition.

It's important to understand that ROT13 offers no real security. It's a very weak form of obfuscation that can be easily reversed by anyone who recognizes the technique or has access to a ROT13 decoder, which are readily available online. 

Consequently, ROT13 should never be used for any serious or sensitive data protection. Its value lies in its simplicity and in situations where only a basic level of obfuscation is sufficient.