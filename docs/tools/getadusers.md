Impacket's `GetADUsers` is a script from the [[Impacket]] suite, a collection of [[Python]] classes for working with network protocols. `GetADUsers` is designed to interact with [[Active Directory]] (AD) environments. It enables the enumeration of user accounts and their attributes from a [[Domain Controller]].

`GetADUsers` can enumerate user accounts in an Active Directory domain, gathering information about each account. The script can retrieve various attributes for each user account, such as the username, description, last logon time, password last set time, and whether the user is required to change their password at the next logon.

`GetADUsers` allows for filtering the results based on specific criteria, which can be useful for targeting particular accounts or for auditing purposes. Here’s a basic example of how `GetADUsers` might be used from the command line:

```bash
python GetADUsers.py <DOMAIN>/<USERNAME>:<PASSWORD>
```

>[!info]
>The script connects to the domain controller and lists user accounts along with selected attributes. You can also use various flags and options to customize the output, such as filtering for users with certain attributes or who have not changed their passwords in a long time.



