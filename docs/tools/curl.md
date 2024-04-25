cURL is a command line tool for transferring data to or from a server using protocols like [[HTTP Protocol|HTTP]] and [[HTTPS Protocol|HTTPS]]. It's widely used in pentesting and can be useful for debugging, testing, and automating tasks that involve the web, file transfers, and website interactions.

It allows you to include sending headers, uploading/downloading files, proxy support, and user authentication.

Some options include:

```bash
-o <file>    # --output: write to file
-u user:pass # --user: authentication
-v   # --verbose: Make curl verbose during operation
-vv  # more verbose
-s   # --silent: don't show progress meter or errors
-S   # --show-error: When used with --silent (-sS), show errors but no progress meter
-i  # --include: include HTTP headers in the output
-I  # --head: header only
-X POST # --request
-L # If the page redirects, follow the link
-F # --form: HTTP POST data for multipart/form-data
-d 'data'
-d @file
-G
-A <str>      # --user-agent
-b name=val   # --cookie
-b FILE       # --cookie
-H "X-Foo: y" # --header
--compressed  # use deflate/gzip
--cacert <file>
--capath <dir>
-E, --cert <cert> # --cert: client certificate file
    --cert-type # der/pem/eng
-k, --insecure # For self-signed certificates
```
