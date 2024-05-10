`SetSPN` is a command-line tool provided by Microsoft that is used to manage [Service Principal Names (SPN)](../security/spns.md) for Windows services in an [Active Directory](../activedirectory/activedirectory.md) environment. SPNs are used in [Kerberos authentication](../activedirectory/kerb.md) to uniquely identify a service instance on a network. The `SetSPN` tool allows administrators to view, modify, and delete SPNs associated with Active Directory service accounts.

`SetSPN` can list the SPNs registered to a specific service account in Active Directory. This is important for ensuring that services are correctly configured for Kerberos authentication. Administrators use `SetSPN` to add new SPNs to a service account. This is necessary when new services are deployed or when services are changed.

If an SPN needs to be changed or if it's incorrectly set, `SetSPN` can modify or remove the SPN from an account. Since incorrect SPN configuration can lead to Kerberos authentication failures, `SetSPN` is often used in troubleshooting related issues.

Some usage examples include assigning an SPN to a service account:

```powershell
setspn -S HTTP/webserver.domain.com DOMAIN\ServiceAccount
```

!!! info
    This command registers the SPN `HTTP/webserver.domain.com` for the specified service account. The `-S` parameter automatically checks for duplicates before adding the SPN.

Or listing SPNs for a service account:

```powershell
setspn -L DOMAIN\ServiceAccount
```

!!! info
    This command lists all SPNs registered to `ServiceAccount`.

You can even remove an SPN:

```powershell
setspn -D HTTP/webserver.domain.com DOMAIN\ServiceAccount
```

!!! info
    This command removes the specified SPN from `ServiceAccount`.

As an example:

In a company, an IT administrator sets up a new web application server `webserver.domain.com` that needs to authenticate users via Kerberos. The administrator assigns an SPN to the service account running the web service using `SetSPN`. This ensures that when users access the web application, the Kerberos authentication process can correctly identify and authenticate the service using the SPN.


