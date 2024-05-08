# Active Directory Federation Services

AD FS (Active Directory Federation Services) is a [Single Sign-On (SSO)](../security/sso.md) solution created by Microsoft. It provides users with authenticated access to applications that aren't capable of using [Integrated Windows Authentication (IWA)](../misc/iwa.md) through [Active Directory (AD)](../activedirectory/activedirectory.md). 

Essentially, AD FS extends the ability to use single sign-on functionality beyond corporate boundaries, making it an essential tool for businesses that use cloud-based services or have partnerships with other organizations.

AD FS allows different organizations to share their identity data securely. When two organizations trust each other's identity systems, they are said to be in a federation, and AD FS manages this trust. Users can authenticate once and gain access to multiple applications, both within and outside their organization. This reduces the need for multiple passwords and login steps.

AD FS acts as an [STS](../security/sts.md), issuing security tokens to clients, which then use these tokens to access different applications. AD FS uses a claims-based access control authorization model to maintain application security. It issues tokens containing a series of claims about a user, like their identity, role, or group membership.

AD FS supports standard web services protocols like [WS-Federation](../protocols/fed.md), [WS-Trust](../misc/trust.md), and [SAML](../misc/saml.md) (Security Assertion Markup Language).

AD FS can be used to provide SSO access to cloud-based services like [Office 365](../misc/o365.md), [Salesforce](../misc/salesforce.md), or any other SAML-compliant application. It simplifies collaboration between businesses by allowing users from one organization to access applications in another without needing separate credentials.

