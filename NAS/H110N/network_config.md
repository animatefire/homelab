# Network Config

## ip addr

1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host noprefixroute
       valid_lft forever preferred_lft forever
2: enp2s0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 40:8d:5c:e4:62:d4 brd ff:ff:ff:ff:ff:ff
    inet 10.0.2.2/24 metric 100 brd 10.0.2.255 scope global dynamic enp2s0
       valid_lft 53460sec preferred_lft 53460sec
    inet6 fe80::428d:5cff:fee4:62d4/64 scope link
       valid_lft forever preferred_lft forever
4: wlp3s0: <BROADCAST,MULTICAST> mtu 1500 qdisc noop state DOWN group default qlen 1000
    link/ether 44:85:00:45:a0:92 brd ff:ff:ff:ff:ff:ff

## ip route

default via 10.0.2.1 dev enp2s0 proto dhcp src 10.0.2.2 metric 100
10.0.2.0/24 dev enp2s0 proto kernel scope link src 10.0.2.2 metric 100
10.0.2.1 dev enp2s0 proto dhcp scope link src 10.0.2.2 metric 100

## sudo cat /etc/netplan/*.yaml

network:
  version: 2
  ethernets:
    enp2s0:
      dhcp4: true