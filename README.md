# aping

A simple utility that sends flood of ICMP ping packets and check the order of incomming packets. Statistic is reported every
5 minutes by default.

## Usage

```
aping <hostip>
```

## Examples

* test of an address without a problem
```
# aping 192.0.2.10
2021-07-15 20:18:56 lost 0 packets in 300 secs {total: 149698}
```

* if there is a problem with packet order or a lost packet, it's reported on standard output

```
# aping 192.0.2.11
2021-07-15 20:24:18 missing 1 pings (last:20702, current:20704)
2021-07-15 20:24:37 lost 1 packets in 60 secs {total: 12315}
2021-07-15 20:25:38 lost 0 packets in 60 secs {total: 12308}
2021-07-15 20:25:56 missing 1 pings (last:40547, current:40549)
```
