Time-based One-Time Password (TOTP) is a widely used algorithm for generating a [[One-Time Password (OTP)]] which is valid for only a short period of time, typically 30 or 60 seconds. TOTPs provide an additional layer of security (often referred to as [[Multi-Factor Authentication (MFA)|two-factor authentication]] or 2FA) for online accounts and transactions. They are used to ensure that, in addition to a username and password, access to an account requires a code that changes at fixed time intervals.

The TOTP algorithm relies on a shared secret key that is known only to the server and the user's device (like a smartphone running a TOTP app). The OTP is generated using the current time as a moving factor, which ensures that the OTP changes at each time step (e.g., every 30 seconds).

The shared secret and the current time are input into a cryptographic hash function (such as [[SHA-1]]), and the output is used to generate the OTP. The generated OTP is typically valid for a short period, after which a new OTP is generated based on the updated current time.

TOTP is implemented in various authentication apps like [[Google Authenticator]], [[Authy]], and others. These apps generate TOTPs that users enter during the login process to access their online accounts. When setting up TOTP for an account, the user scans a QR code or enters a setup key to synchronize the shared secret key between their app and the server.

Each time the user logs in, they must provide the current OTP from their app, along with their regular username and password.

Since each OTP is only valid for a short period, even if an OTP is intercepted by an attacker, it quickly becomes useless. TOTPs offer protection against [[phishing]], as the password is constantly changing and known only to the user and the server.

