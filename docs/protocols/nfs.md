It is a [[client]]/[[server]] system that allows users to access files across a network and treat them as if they resided in a local file directory. It has the same purpose as [[Server Message Block|SMB]] but it cannot talk to SMB.

The NFS protocol has no mechanism for authentication or authorization. The authorization is taken from the available information of the file system where the server is responsible for translating the user information supplied by the client to that of the file system and converting the corresponding authorization information as correctly as possible into the syntax required by UNIX.

The most common authentication is via UNIX **`UID`****/****`GID`** **and** **`group memberships`**, which is why this syntax is most likely to be applied to the NFS protocol. 

One problem is that the client and server do not necessarily have to have the same mappings of UID/GID to users and groups. No further checks can be made on the part of the server. This is why NFS should only be used with this authentication method in trusted networks.