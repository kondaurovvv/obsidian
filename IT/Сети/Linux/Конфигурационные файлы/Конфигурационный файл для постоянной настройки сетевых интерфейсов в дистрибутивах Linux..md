
Это основной конфигурационный файл для постоянной настройки сетевых интерфейсов в дистрибутивах Linux.
```bash
/etc/network/interfaces
```

```bash
# Static config for eth0
auto eth0
iface eth0 inet static
		hwaddress ether 00:00:aa:aa:01:01
        address 192.168.1.1
        netmask 255.255.255.0
		gateway шлюз (ваш роутер)
        broadcast 192.168.1.255
        up echo nameserver 8.8.8.8 > /etc/resolv.conf
```

## Перезапустить сетевую службу.


```bash
/etc/init.d/networking restart
```

```bash
systemctl restart networking
```

```bash
systemctl restart NetworkManager
```

```bash
service networking restart
```

#it #сети #linux #конфигурационный_файл #сетевая_служба