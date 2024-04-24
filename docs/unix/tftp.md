icon:fontawesome/solid/terminal

# Tftp

Simple file transfer protocol used for transferring files between systems over a network, often used for bootstrapping network devices or transferring configuration files.

## Examples

For TFTP-server check atftp.

##### Test for TFTP

If error occurs this means the server is running TFTP.

```bash
$ tftp 10.10.10.1 69

tftp> get nonexistingfile.txt
Error code 4: Transfer mode not supported.
```

## References

- [Scan.shadowserver.org](https://scan.shadowserver.org/tftp/)
