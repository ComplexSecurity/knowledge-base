icon:material/apple

# Networkquality

Command-line tool on macOS that measures the internet connection quality in terms of upload and download speeds and responsiveness.

## Usage

```bash
networkQuality [-C <configuration_url>] [-c] [-h] [-I <interfaceName>] [-s] [-v]
```

## Flags

```bash
    -C: override Configuration URL
    -c: Produce computer-readable output
    -h: Show help (this message)
    -I: Bind test to interface (e.g., en0, pdp_ip0,...)
    -s: Run tests sequentially instead of parallel upload/download
    -v: Verbose output
```

## Examples

```bash
$ networkQuality -v
==== SUMMARY ====
Upload capacity: 7.531 Mbps
Download capacity: 230.944 Mbps
Upload flows: 20
Download flows: 12
Responsiveness: Low (42 RPM)
Base RTT: 1075
Start: 13/01/2022, 10:32:07
End: 13/01/2022, 10:32:30
OS Version: Version 12.1 (Build 21C52)
```

## References

- [Support.apple.com - Test Wi-Fi networks with Apple Network Responsiveness](https://support.apple.com/kb/HT212313)
