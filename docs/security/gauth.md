Google Authenticator is a software-based authentication tool that provides a [Multi-Factor Authentication (MFA)|two-factor authentication (2FA)]() service. It's commonly used to add an additional layer of security to online accounts beyond just a username and password. The app generates [Time-based One-Time Password (TOTP)|time-based one-time passwords (TOTPs)]() that the user must enter in addition to their regular password to gain access to an account.

The app generates a six to eight-digit passcode which changes every 30 seconds. This code is used for the second step of the verification process. The app doesn't require an internet connection to generate codes. It works offline, which is beneficial in areas with unreliable network connectivity.

Setting up an account with Google Authenticator typically involves scanning a QR code provided by the service with which you are setting up 2FA. This QR code securely transfers the shared secret key used to generate the TOTPs.

The app can store and manage codes for multiple accounts, making it convenient for users with several 2FA-enabled accounts.

The process is:

- When you enable 2FA on an account, you'll have the option to use an authenticator app. If you choose Google Authenticator, you'll typically scan a QR code using the app.
- This QR code adds your account to the app and sets up a unique, shared secret key between the server and the app.
- When you log into the account, after entering your password, you'll be prompted to enter the code from Google Authenticator.
- Open the app to see the currently valid code for that account. This code changes every 30 seconds.

By requiring a second form of verification, Google Authenticator significantly enhances account security, protecting against password theft and unauthorized access. Even if a password is compromised, an attacker would still need the TOTP from Google Authenticator to access the account.