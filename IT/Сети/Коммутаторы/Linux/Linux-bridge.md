
## Установка.

```bash
apt install bridge-utils -y
```

## Команды bridge-utils

Проверка установки.
```bash
brctl --version

which brctl
```

Проверка текущих бриджей.
 ```bash
 brctl show
 ```

Создание бриджа.
```bash
brctl addbr <имя бриджа>
```

Добавление интерфейсов в бридж.
 ```bash
 brctl addif <имя бриджа> <имя адаптера>
 ```

Поднятие бриджа (включение).
 ```
 ip link set <имя бриджа> up
 
 ifconfig <имя бриджа> up
 ```

Выключение бриджа.
```bash
ip link set <имя бриджа> down

ifconfig <имя бриджа> up
```

Проверка статуса бриджа.
```bash
ip link show <имя бриджа>

ifconfig
```

Вывести таблицу MAC адресов.
```bash
brctl showmacs <имя бриджа>
```
- **port no** — номер порта бриджа (соответствует интерфейсу eth1/eth2/eth3)
- **mac addr** — MAC-адрес
- **is local?**
   - `yes` — MAC-адрес самого бриджа (локальный)
   - `no` — MAC-адрес подключенного устройства (это MAC-адреса ваших узлов rbr-node-01/02/03)
- **ageing timer** — время в секундах, сколько осталось до удаления записи (если записи не будет обновляться)

Изменение времени жизни MAC-адресов.
```bash
brctl setageing <имя бриджа> <время в секундах>
```

Включение STP (Spanning Tree Protocol).
```bash
brctl stp <имя бриджа> on
```

Отключение STP (Spanning Tree Protocol).
```bash
brctl stp <имя бриджа> off
```

Удаление интерфейса из бриджа.
```bash
brctl delif <имя бриджаЮ <имя адаптера>
```

Удаление бриджа.
```bash
ip link set <имя бриджа> down

brctl delbr <имя бриджа>
```

#it #сети #коммутаторы #linux #bridge-utils #brctl