WPScan is a free, for non-commercial use, black box [WordPress](../web/wordpress.md) vulnerability scanner that can be used to scan WordPress websites for security vulnerabilities. It's a command-line tool written in Ruby, and it's widely used by WordPress administrators, security professionals, and ethical hackers to assess the security of WordPress sites.

WPScan can enumerate WordPress usernames, which can be used in [brute force attacks](../security/brute.md). It can identify the plugins and themes installed on a WordPress site, along with their versions. This is useful for finding potential vulnerabilities associated with specific versions.

WPScan has a database of known WordPress vulnerabilities and can check a site against this database to identify known security issues. WPScan can perform password brute force attacks to test the strength of user passwords. It can detect which WordPress version is being used and whether it's up-to-date or vulnerable.

WPScan can check for vulnerabilities in the Timthumb script, which was commonly used in older WordPress installations.

To scan a WordPress site, you can use the command:

```bash
wpscan --url [website-url]
```

To enumerate users:

```bash
wpscan --url [website-url] --enumerate u
```

To enumerate plugins:

```bash
wpscan --url [website-url] --enumerate p
```

To enumerate themes:

```bash
wpscan --url [website-url] --enumerate t
```

You can also perform a password attack:

```bash
wpscan --url [website-url] --passwords [path-to-password-file]
```

!!! info
    WPScan's vulnerability database is updated regularly, so it's important to update WPScan frequently to ensure it has the latest information.
