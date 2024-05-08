WEP (Wired Equivalent Privacy) is a security protocol that was designed to provide a wireless local area network ([WLAN](../networking/wlans.md)) with a level of security and privacy comparable to what is usually expected of a wired LAN.

It was part of the original IEEE 802.11 standard ratified in 1997. However, WEP has several significant weaknesses and is considered deprecated and insecure in modern networking.

WEP uses the RC4 stream cipher for encryption. It encrypts data transmitted over the WLAN to protect it from eavesdropping. A major weakness of WEP is the use of static encryption keys that are shared among devices on the network. Once the key is known, it can be used to decrypt all traffic encrypted with it.

WEP supports key sizes of 40 bits and 104 bits (often referred to as 64-bit and 128-bit, respectively, including a 24-bit initialization vector). Key management in WEP is poor, as keys need to be manually set and are not regularly changed.

WEP supports two types of authentication - Open System authentication and Shared Key authentication. Both methods have significant security weaknesses. WEP uses a 24-bit IV, which is quite small. This leads to frequent reuse of the same IV, which, combined with other flaws, makes it easier to crack the encryption key.

WEP is vulnerable to several types of attacks, most notably key recovery attacks that can extract the WEP key from captured packets. Tools like [Aircrack-ng](../tools/aircrack-ng.md) made it possible to crack WEP keys within minutes.

Due to its vulnerabilities, WEP was superseded by [Wi-Fi Protected Access (WPA)](../protocols/wpa.md) in 2003 and later WPA2. Both provide stronger security mechanisms. Despite its weaknesses, WEP was still used in some older or legacy systems that have not been updated to support newer security protocols.

Security experts and industry standards strongly advise against using WEP due to its vulnerabilities. It's considered ineffective at providing meaningful WLAN security. While now outdated, WEP was one of the first attempts to secure wireless networks, playing a significant role in the history of WLAN development.
