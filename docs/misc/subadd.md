Sub-addressing in email, also known as "plus addressing," is a feature that allows users to extend their email addresses using a '+' symbol followed by a tag or keyword. This extension creates variations of the main email address, which are all delivered to the same mailbox. Sub-addressing is particularly useful for organizing incoming mail and for identifying sources of spam.

Suppose your primary email address is `user@example.com`. With sub-addressing, you can extend this address in the following way:

- `user+shopping@example.com`
- `user+newsletters@example.com`
- `user+friends@example.com`

All emails sent to these addresses will be delivered to the inbox of `user@example.com`. However, the part after the '+' symbol allows for easy identification and management of incoming emails.

By using different sub-addresses for different purposes or registrations (like online shopping, forums, newsletters), you can easily organize incoming emails into folders or apply specific rules based on the sub-address used. If you start receiving spam on a sub-address, it's easier to identify which service or registration may have compromised your email address or sold it to spammers.

Sub-addressing can be used to quickly create "disposable" email addresses for one-time use without having to set up an actual new account.

In the context of web application penetration testing, sub-addressing (or plus addressing) in emails can be used as a technique for testing and identifying security vulnerabilities, particularly in areas related to user account management, email validation, and information leakage.

You can use sub-addressing to test how the web application handles email addresses with a '+' character. Check if the application accepts such emails and correctly sends messages to them. This can reveal how robust the application's input validation is.

If the application requires unique emails for each account, sub-addressing can be used to create multiple accounts with what is essentially the same email address. For example, `user@example.com`, `user+test1@example.com`, and `user+test2@example.com` will all typically deliver to `user@example.com`.

By registering with a sub-address, you can check if the application mishandles the part after the '+'. For instance, some applications might not properly parse the email address, leading to issues in email delivery or account verification.

You can also potentially identify third-party sharing by registering on the application with a unique sub-address and monitor the inbox for emails sent to that address. If you start receiving emails (especially spam) not related to the original application, it could indicate that your email address has been shared with or leaked to third parties.

While less common, you might test for injection vulnerabilities by including special characters or payloads in the sub-address part to see how the server handles and sanitizes these inputs. However, this is more of an edge case and less likely to yield significant results compared to other testing methods.

Sub-addressing might be used in account enumeration testing. By using different sub-addresses and observing the application's responses, you might be able to infer the existence of certain user accounts.
