icon:material/apple

# Ditto

Command-line utility on macOS used to copy files and directories while preserving file attributes and permissions.

## Usage

```bash
ditto [ <options> ] src [ ... src ] dst
```

## Flags

```bash
<options> are any of:
-h                         print full usage
-v                         print a line of status for each source copied
-V                         print a line of status for every file copied
-X                         do not descend into directories with a different device ID

-c                         create an archive at dst (by default CPIO format)
-x                         src(s) are archives
-z                         gzip compress CPIO archive
-j                         bzip2 compress CPIO archive
-k                         archives are PKZip
--keepParent               parent directory name src is embedded in dst_archive
--arch archVal             fat files will be thinned to archVal
                            multiple -arch options can be specified
                            archVal should be one of "ppc", "i386", etc
--bom bomFile              only objects present in bomFile are copied
--norsrc                   don't preserve resource data
--noextattr                don't preserve extended attributes
--noqtn                    don't preserve quarantine information
--noacl                    don't preserve ACLs
--sequesterRsrc            copy resources via polite directory (PKZip only)
--nocache                  don't use filesystem cache for reads/writes
--hfsCompression           compress files at destination if appropriate
--nopreserveHFSCompression don't preserve HFS+ compression when copying files
--zlibCompressionLevel num use compression level 'num' when creating a PKZip archive
--password                 request password for reading from encrypted PKZip archive
```

## Examples

##### Using ditto to copy files/folders

```bash
ditto source destination
```

##### Copy without metadata

```bash
ditto -V --nosrc ~/Sample/Folder /Volumes/NoMetadataBackups
```

## References

- [ss64.com - ditto](https://ss64.com/osx/ditto.html)
- [OSXdaily.com - Use ditto to Copy Files & Directories Intelligently from the Mac Terminal](https://osxdaily.com/2014/06/11/use-ditto-copy-files-directories-mac-command-line/)
