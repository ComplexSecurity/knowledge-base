Aircrack-ng is a network software suite consisting of a detector, packet sniffer, [WEP](../protocols/wep.md) and [WPA](../protocols/wpa.md)/[WPA2](../protocols/wpa2.md)-PSK cracker, and analysis tool for 802.11 [wireless LANs](). It works with any wireless network interface controller whose driver supports raw monitoring mode and can sniff 802.11a, 802.11b, and 802.11g traffic.

The primary use of Aircrack-ng is to crack WEP and WPA/WPA2-PSK keys. It implements standard FMS attacks along with some optimizations like KoreK attacks, as well as the PTW attack to make its attacks more potent.

Aircrack-ng can capture network packets and then analyze them to recover wireless keys. It is capable of capturing packets that are not encrypted, as well as those encrypted with WEP, WPA, or WPA2.

Beyond cracking, Aircrack-ng can be used for network auditing. It can test network security, detect network connections, and devices, and assess the performance and strength of a network. Aircrack-ng suite includes several tools - `airmon-ng` (puts your card into monitor mode), `airodump-ng` (packet capturing), `aireplay-ng` (packet injection), `aircrack-ng` (WEP and WPA/WPA2 cracking), and others.

For WEP, Aircrack-ng uses statistical attacks to deduce the encryption key. The time it takes to crack WEP keys can vary depending on the number of network packets captured. Cracking WPA and WPA2 requires a different approach. It usually involves capturing a handshake process between a client and an access point and then performing a brute-force attack or dictionary attack to guess the passphrase.

