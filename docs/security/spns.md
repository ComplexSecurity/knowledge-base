Service Principal Names (SPNs) in Microsoft Windows are unique identifiers assigned to each service instance on a network. They are used in [Kerberos authentication]() to associate a service instance with a service logon account. This association is crucial for Kerberos to correctly authenticate clients accessing network services.

An SPN uniquely identifies a service instance in a domain, ensuring that Kerberos authentication can uniquely target that service when a client requests access. SPNs have a specific format, usually as `serviceType/host:port/serviceName`. For example, a typical SPN for a web service might be `HTTP/webserver.domain.com`.

When a client wants to access a service in a Windows network, it requests a [Kerberos Tickets|Kerberos ticket]() for the SPN of that service. The [Domain Controller]() then uses the SPN to find the service's account in the [Active Directory]() and issue an appropriate ticket.

Imagine a SQL Server named `sqlserver1` in the domain `company.com` running under the service account `SQLService`. The SPN for this SQL Server might look like:

```bash
MSSQLSvc/sqlserver1.company.com:1433
```

This SPN includes:

- The service type: `MSSQLSvc`
- The host: `sqlserver1.company.com`
- The port: `1433` (the default port for SQL Server)

!!! info
    When a client application tries to connect to this SQL Server instance using Windows Authentication, the Kerberos protocol uses this SPN to authenticate and securely negotiate the connection.


