# iptables-management
A collection of basic, colorful shell tools to make iptables management less painful.

The two scripts, `tadd` and `trm` are used to allow or remove exclusive single port access to specific IPs on the host machine. This is of particular use when using applications that punch holes in your firewall such as Docker. In such a situation, you are likely to have a use where only one machine on your network should have exclusive access to a specific port on another machine.

# Usage
The scripts are extremely simple and are used as follows:
```
tadd <ip> <port>
trm <ip> <port>
```

# Example
If we were to use the following:
```
tadd 192.168.1.5 2040
```
then only the machine on IP `192.168.1.5` would be able to directly access port `2040` on the machine we used the `tadd` script on.

To remove the rule, we would use the following command:
```
trm 192.168.1.5 2040
```
