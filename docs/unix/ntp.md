icon:fontawesome/solid/terminal

# Ntp

Used to synchronize the system clock with internet time servers for accurate timekeeping.

## Examples

##### NTP-Mode 6

```bash
$ ntpq -c rv 10.10.10.1

associd=0 status=0615 leap_none, sync_ntp, 1 event, clock_sync,
processor=, system="/", leap=00, stratum=4, precision=-17,
rootdelay=84.332, rootdisp=60.253, refid=10.204.32.110,
reftime=e25a6793.087b11c2  Mon, May  4 2020 12:06:11.033,
clock=e25a67a9.7b8ae150  Mon, May  4 2020 12:06:33.482, peer=13389, tc=6,
mintc=3, offset=+2.729, frequency=+10.297, sys_jitter=14.127,
clk_jitter=1.646, clk_wander=0.021
```

##### Simply synchronize time

```bash
sudo service ntp stop
sudo ntpd -gq
sudo service ntp start
```

## References

- [Linux.die.net](https://linux.die.net/man/8/ntpd)
