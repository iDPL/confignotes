confignotes
===========

Configuration notes for various machines

The items catalogued here are should also part of the configuration code in the idplconfig roll.

TCP sysctl configuration
See: https://www.kernel.org/doc/Documentation/networking/ip-sysctl.txt  and
https://www.kernel.org/doc/Documentation/sysctl/net.txt 
for detailed description of these variables

| systctl variable | CentOS default |  iDPL Configuration |   Notes
|------------------|----------------|---------------------| ------- | 
net.core.netdev_max_backlog | 1000 | 250000 |  increase number of allowed outstanding receive packets |
net.ipv4.tcp_no_metrics_save| 0 | 1 | do not cache previous tcp parameters |
net.ipv4.tcp_congestion_control| cubic | cubic |
net.ipv4.tcp_mtu_probing | 0 | 1 |  find minimum mtu between two endpoints | 
net.core.rmem_max| 124928 | 268435456 |  256MB for large Bandwidth-Delay-Product networks |
net.core.wmem_max| 124928 | 268435456 |  256MB for large Bandwidth-Delay-Product networks |
net.ipv4.tcp_rmem| 4096 87380 4194304 |4096 65536 134217728 | max TCP window size to 128MB |
net.ipv4.tcp_wmem| 4096 16384 4194304|4096 65536 134217728 |  max TCP window size to 128MB |

