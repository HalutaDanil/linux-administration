## Задай название машины вида user-1.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/hostnamectl.png)
- Использование команды `hostnamectl set-hostname` для смены названия машины

## Установи временную зону, соответствующую твоему текущему местоположению.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/timedatectl.png?ref_type=heads)
- Использование команды `timedatectl set-timezone` для выбора временной зоны

## Выведи названия сетевых интерфейсов с помощью консольной команды.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/iplink.png?ref_type=heads)
- Использование команды `ip link` для вывода всех сетевых интерфейсов

- lo (loopback) - это виртуальный сетевой интерфейс, который создается операционной системой и работает по кругу, то есть отправленные пакеты возвращаются в место отправки, таким образом замыкая себя. Это применяется при тестировании сетевого соединения, обращении к локальным сервисам и т.д.

## Используя консольную команду, получи ip адрес устройства, на котором ты работаешь, от DHCP-сервера.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/ipa_and_dhclient.png?ref_type=heads)
- Использование команды `dhclient` для ручного получения ответа от DHCP и команды `ip a` для вывода всех сетевых интерфейсов и ip-адресов

- DHCP - Dynamic Host Configuration Protocol.

## Определи и выведи на экран внешний ip-адрес шлюза (ip) и внутренний IP-адрес шлюза, он же ip-адрес по умолчанию (gw).

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/iproute.png?ref_type=heads)
- Использование команд `ip route, hostname -I, curl ifconfig.me` для вывода внешних и внутренних ip-адресов шлюзов

## Задай статичные (заданные вручную, а не полученные от DHCP-сервера) настройки ip, gw, dns (используй публичный DNS-серверы, например 1.1.1.1 или 8.8.8.8).

- Открыл файл с расширением .yaml по пути /etc/netplan/, который содержит конфиг сетевых настроек.
- Заменил некоторые строчки и добавил свои настройки.
- Прописал команду `sudo netplan apply`, чтобы утилита netplan приняла изменения.
- Перезагрузил ВМ командой `reboot`.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/netplan.png?ref_type=heads)
- Вид сетевого конфигурационного файла

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/result_network_setting.png?ref_type=heads)
- Результат настройки сети

## Успешно пропингуй удаленные хосты 1.1.1.1 и ya.ru.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/ping.png?ref_type=heads)
- Пинг удаленных хостов с 0% packet loss
