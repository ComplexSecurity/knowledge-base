Side-channel attacks are a type of security exploit that target the implementation of a computer system rather than weaknesses in the actual algorithms themselves. These attacks are based on information gained from the physical implementation of a system, such as timing information, power consumption, electromagnetic leaks, or even sounds. 

Unlike other methods, side-channel attacks don't directly attack the cryptographic algorithm but rather exploit weaknesses in how the system executes the algorithm.

Some key types include:

1. **Timing Attacks**: These involve measuring the time it takes to execute cryptographic operations. Differences in timing can be used to infer information about the secret data. For example, if certain operations take longer when a specific bit in the key is set, an attacker might deduce the value of these bits by measuring the time of execution.
2. **Power Analysis Attacks**: These look at the power consumption of a device during cryptographic processing. Different operations consume different amounts of power, and this can be used to deduce information about the secret keys.
3. **Electromagnetic Attacks**: Similar to power analysis, these attacks measure the electromagnetic emissions of a device. By analyzing these emissions, an attacker can potentially extract secret keys or other sensitive information.
4. **Acoustic Cryptanalysis**: This involves analyzing sounds emitted by a device, which can vary based on the operations being performed. Even subtle differences in sound can reveal information about what the device is processing.

One classic example of a side-channel attack is the [RSA (Rivest-Shamir-Adleman)|RSA]() timing attack demonstrated by Paul Kocher in the late 1990s. In this attack:

- Kocher showed that by measuring the amount of time a system takes to decrypt messages using the RSA algorithm, an attacker could work out the private key.
- RSA decryption involves modular exponentiation, where the exponent is the secret key. The time taken for this operation can vary slightly depending on the value of the key.
- By carefully measuring the decryption times for many different encrypted messages and performing statistical analysis, Kocher was able to recover the private key.

