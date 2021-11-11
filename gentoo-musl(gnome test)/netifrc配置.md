## 注意 ##

Musl 目前安装 Network Mananger 会引入 `rust` 和 `spidermonkey` 两个包，前一个包能够正常编译通过，但后一个会因为[bug](https://bugs.gentoo.org/822822)造成编译失败，所以，目前建议不要使用 `NetworkManager` ，使用 netifrc 。

## 在虚拟机里简要配置 `netifrc` 联网 ##

1. `ln -s /etc/init.d/net.lo /etc/init.d/net.enp1s0`
2. `nano /etc/conf.d/net`
3. 配置：
```
config_enp1s0="192.168.122.2 netmask 255.255.255.0"
routes_enp1s0="default via 192.168.122.1"
dns_servers_enp1s0="8.8.8.8"
```
4. `rc-update add net.enp1s0 default`

重启后，实现静态网络链接。