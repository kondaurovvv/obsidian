Идентификация пользователей (UID)

Классификация OC:
- Однопользовательские однозадачные:
	- MS-DOS.
- Однопользовательские многозадачные:
	- Windows 95.
- Многопользовательские многозадачные:
	- Все современные системы (Linux, UNIX, Windows 10).

Имена пользователей:
- Строка, максимальная длина 32 символа;
- Может содержать любые символы (кроме двоеточия и символа новой строки);
- Короткий и легко запоминаемый псевдоним.

UID (User identifer):
- Число от 0 д о 2<sup>32</sup>;
- Идентификатор пользователя;
- OC определяет пользователя по UID.

Два типа пользователей:
- root (UID 0):
	- Не имеет ==НИКАКИХ== ограничений в LINUX;
- Все остальные (UID не 0):
	- Служебные пользователи (MySQL, NGINX):
		- Демон - компьютерная программа в системах класса UNIX, запускаемая самой системой и работающая в фоновом режиме без прямого взаимодействия с пользователем.
	- Обычные (люди).

/etc/passwd
```
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin
irc:x:39:39:ircd:/run/ircd:/usr/sbin/nologin
_apt:x:42:65534::/nonexistent:/usr/sbin/nologin
nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin
systemd-network:x:998:998:systemd Network Management:/:/usr/sbin/nologin
dhcpcd:x:100:65534:DHCP Client Daemon:/usr/lib/dhcpcd:/bin/false
tss:x:101:103:TPM software stack:/var/lib/tpm:/bin/false
systemd-timesync:x:991:991:systemd Time Synchronization:/:/usr/sbin/nologin
messagebus:x:990:990:System Message Bus:/nonexistent:/usr/sbin/nologin
sshd:x:989:65534:sshd user:/run/sshd:/usr/sbin/nologin
dnsmasq:x:999:65534:dnsmasq:/var/lib/misc:/usr/sbin/nologin
avahi:x:102:107:Avahi mDNS daemon:/run/avahi-daemon:/usr/sbin/nologin
speech-dispatcher:x:103:29:Speech Dispatcher:/run/speech-dispatcher:/bin/false
usbmux:x:104:46:usbmux daemon:/var/lib/usbmux:/usr/sbin/nologin
cups-pk-helper:x:105:108:user for cups-pk-helper service:/nonexistent:/usr/sbin/nologin
fwupd-refresh:x:988:988:Firmware update daemon:/var/lib/fwupd:/usr/sbin/nologin
geoclue:x:106:110::/var/lib/geoclue:/usr/sbin/nologin
gnome-remote-desktop:x:987:987:GNOME Remote Desktop:/var/lib/gnome-remote-desktop:/usr/sbin/nologin
saned:x:107:111::/var/lib/saned:/usr/sbin/nologin
polkitd:x:986:986:User for polkitd:/:/usr/sbin/nologin
rtkit:x:108:112:RealtimeKit:/proc:/usr/sbin/nologin
colord:x:109:113:colord colour management daemon:/var/lib/colord:/usr/sbin/nologin
Debian-gdm:x:110:114:Gnome Display Manager:/var/lib/gdm3:/bin/false
name:x:1000:1000:Bulka,,,:/home/name:/bin/bash

```

root:x:0:0:root:/root:/bin/bash
- root - псевдоним (логин);
- x - признак того, что пароль зашифрован и хранится в отдельном файле `/etc/shadow`;
- 0 - UID (User identifer);
- 0 - GIT (Group IDentifier);
- root - комментарий обычно здесь пишут полное имя пользователя или описание.
- /root - домашний каталог пользователя. ;
- /bin/bash - командная оболочка (shell), которая запускается при входе в систему.

/etc/group
```
root:x:0:
daemon:x:1:
bin:x:2:
sys:x:3:
adm:x:4:
tty:x:5:
disk:x:6:
lp:x:7:
mail:x:8:
news:x:9:
uucp:x:10:
man:x:12:
proxy:x:13:
kmem:x:15:
dialout:x:20:
fax:x:21:
voice:x:22:
cdrom:x:24:bulka
floppy:x:25:bulka
tape:x:26:
sudo:x:27:
audio:x:29:bulka
dip:x:30:bulka
www-data:x:33:
backup:x:34:
operator:x:37:
list:x:38:
irc:x:39:
src:x:40:
shadow:x:42:
utmp:x:43:
video:x:44:bulka
sasl:x:45:
plugdev:x:46:bulka
staff:x:50:
games:x:60:
users:x:100:bulka
nogroup:x:65534:
systemd-journal:x:999:
systemd-network:x:998:
crontab:x:997:
input:x:996:
sgx:x:995:
clock:x:994:
kvm:x:993:
render:x:992:
netdev:x:101:bulka
scanner:x:102:saned,bulka
tss:x:103:
systemd-timesync:x:991:
messagebus:x:990:
_ssh:x:104:
ssl-cert:x:105:
bluetooth:x:106:bulka
avahi:x:107:
lpadmin:x:108:bulka
pipewire:x:109:
fwupd-refresh:x:988:
geoclue:x:110:
gnome-remote-desktop:x:987:
saned:x:111:
polkitd:x:986:
rtkit:x:112:
colord:x:113:
Debian-gdm:x:114:
bulka:x:1000:
```

