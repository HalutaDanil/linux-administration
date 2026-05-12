---

# Task Task

## Установи Ubuntu 20.04 Server LTS без графического интерфейса. (Используем программу для виртуализации — VirtualBox)

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/task1.png)
- вывод команды `cat /etc/issue`

---

# Task Task

## Создай пользователя, отличного от созданного при установке. Пользователь должен быть добавлен в группу `adm`.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/task2-createuser-and-appendadm.png)
- использование команд `sudo adduser newuser` и `sudo usermod -aG adm newuser`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/task2-passwd.png)
- вывод команды `cat /etc/passwd`

---

# Task Task

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

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/netplan.png?ref_type=heads)
- Вид сетевого конфигурационного файла

## Перезагрузи виртуальную машину. Убедись, что статичные сетевые настройки (ip, gw, dns) соответствуют заданным в предыдущем пункте.

- Перезагрузил ВМ командой `reboot`.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/result_network_setting.png?ref_type=heads)
- Результат настройки сети

## Успешно пропингуй удаленные хосты 1.1.1.1 и ya.ru.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/ping.png?ref_type=heads)
- Пинг удаленных хостов с 0% packet loss

---

# Task Task

## Обнови системные пакеты до последней на момент выполнения задания версии.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/task4.png?ref_type=heads)
- Использование команды `apt update` и команды `apt upgrade`

---

# Task Task

## Разреши пользователю, созданному в Part 2,выполнять команду sudo.

- использовал команду `sudo usermod -aG sudo newuser`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/task5.png?ref_type=heads)
- Изменение `hostname`, созданным пользователей

- Команда `sudo` дает пользователю временные права суперпользователя для выполнения задач, для доступа к которым нужны административные права.

---

# Task Task

## Настрой службу автоматической синхронизации времени.

- использовал команду `sudo timedatectl set-ntp true`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/task6.png?ref_type=heads)
- Использование команды `timedatectl` и команды `date`

---

# Task Task

## Установи текстовые редакторы VIM (+ любые два по желанию NANO, MCEDIT, JOE и т. д.)

- Редакторы VIM, NANO уже были установлены, а вот MCEDIT пришлось установить, проверив обновления `sudo apt update`, командой `sudo apt install mcedit`.

## Используя каждый из трех выбранных редакторов, создай файл test_X.txt, где X — название редактора, в котором создан файл. Напиши в нём свой никнейм, закрой файл с сохранением изменений.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/vim_aemonhul.png?ref_type=heads)
- Вид из редактора VIM

- Для выхода с сохранением нажал `esc`, далее `:` и ввел `wq`.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/mcedit_aemonhul.png?ref_type=heads)
- Вид из редактора MCEDIT

- Для выхода с сохранением нажал `esc`, далее `2`, снова `esc` и `0`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/nano_aemonhul.png?ref_type=heads)
- Вид из редактора NANO

- Для выхода с сохранением нажал `ctrl + O`, а после `ctrl + X`

## Используя каждый из трех выбранных редакторов, открой файл на редактирование, отредактируй файл, заменив никнейм на строку «21 School 21», закрой файл без сохранения изменений.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/vim_School21.png?ref_type=heads)
- Вид из редактора VIM

- Для выхода без сохранения нажал `esc`, далее `:` и ввел `q!`.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/mcedit_School21.png?ref_type=heads)
- Вид из редактора MCEDIT

- Для выхода без сохранения нажал `esc`, далее `0`, а на вопрос, хочу ли я сохранить изменения, нажал `enter` на `no`.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/nano_School21.png?ref_type=heads)
- Вид из редактора NANO

- Для выхода без сохранения нажал `ctrl + X`, а на вопрос, хочу ли я сохранить изменения, ввел `n`.

## Используя каждый из трех выбранных редакторов, отредактируй файл ещё раз (по аналогии с предыдущим пунктом), а затем освой функции поиска по содержимому файла (слово) и замены слова на любое другое.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/vim_search.png?ref_type=heads)
- Поиск вхождения слова в редакторе VIM с помощью команды `/word`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/vim_replace.png?ref_type=heads)
- Замена `old word` на `new word` в редакторе VIM с помощью команды `:s/old/new/g`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/mcedit_search.png?ref_type=heads)
- Поиск вхождения слова в редакторе MCEDIT с помощью нажатия клавиш `esc + 7`, ввода интересующего слова и нажатия `enter`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/mcedit_replace_1.png?ref_type=heads)
- Первое меню для замены слова в редакторе MCEDIT, открывается нажатием клавиш `esc + 4`, затем `enter`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/mcedit_replace_2.png?ref_type=heads)
- Второе меню для замены слова в редакторе MCEDIT для подтверждения замены и выбора количества слов для замены, выбор осуществляется клавишей `enter`.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/mcedit_replace_3.png?ref_type=heads)
- Результирующее скрин замены слова в редакторе MCEDIT, где произошла замена.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/nano_search.png?ref_type=heads)
- Поиск вхождения слова в редакторе NANO с помощью нажатия клавиш `ctrl + w`, ввода интересующего слова и нажатия `enter`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/nano_replace_1.png?ref_type=heads)
- Первое меню для замены слова в редакторе NANO для ввода слова, которое необходимо заменить. Активируется нажатием `ctrl + \`, после ввода `enter`.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/nano_replace_2.png?ref_type=heads)
- Второе меню для замены слова в редакторе NANO для ввода слова, на которое необходимо заменить. После ввода `enter`.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/nano_replace_3.png?ref_type=heads)
- Третье меню для замены слова в редакторе NANO для подтверждения замены и выбора количества слов для замены, выбор осуществляется вводом буквы, которая стоит рядом с интересующим пунктом. После ввода `enter`.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/nano_replace_4.png?ref_type=heads)
- Результирующее скрин замены слова в редакторе NANO, где произошла замена.

---

# Task Task

## Установи службу SSHd.

- проверил обновления перед установкой командой `sudo apt update`
- Ввел команду `sudo apt install openssh-server`.

## Добавь автостарт службы при загрузке системы.

- Проверил состояние служб `ssh.service` и `sshd.service` с помощью команд `sudo systemctl status ssh.service` и `sudo systemctl status sshd.service`. Обе службы находились в состоянии `inactive (dead)`.
- Запустил службу `OpenSSH` командой `sudo systemctl start ssh.service`.
- Включил автозапуск службы при загрузке системы командой `sudo systemctl enable ssh.service`.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/check_status_ssh.service.png?ref_type=heads)
- Проверка статуса `ssh.service`

## Перенастрой службу SSHd на порт 2022.

- Открыл файл `/etc/ssh/sshd_config` с правами суперпользователя и раскомментировал строчку `Port 22` и изменил значение `22` на `2022`.
- После, рестартнул службу `OpenSSH` командой `sudo systemctl restart sshd`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/check_port.png?ref_type=heads)
- Проверка изменения порта через `sudo systemctl status sshd`

## Используя команду ps, покажи наличие процесса sshd. Для этого к команде нужно подобрать ключи.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/ps.png?ref_type=heads)
- Вывод команды `ps -C sshd -f`

- Команда `ps` предназначена для просмотра запущенных процессов, она демонстрирует идентификационные номер процесса `PID` и многое другое. Ключ `-C` используется для поиска процесса по имени исполняемого файла, в нашем случае - это `sshd`. Ключ `-f` добавляет полный формат данных, связанных с процессом.

## Перезагрузи систему.

- Использовал команду `reboot`

## `netstat -tan`

- Проверил обновления пакетов командой `sudo apt update`
- Установил `net-tools` командой `sudo apt install net-tools`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/netstat.png?ref_type=heads)
- Вывод команды `netstat -tan`

- `-t` - ограничить вывод tcp-сокетами.
- `-a` - показать все сокеты во всех состояниях.
- `-n` - отключить резолвинг, чтобы выводить не в человекочитаемом формате, а в числовом.

- `Proto` - транспортные протоколы.
- `Recv-Q` - количество байт, которые получило ядро, но они еще не прочитаны приложением.
- `Send-Q` - количество байт, переданных приложением ядру, но еще не подтвержденных удаленной стороной.
- `Local Address` - локальный адрес и порт, к которым привязан сокет.
- `Foreign Address` - удаленный адрес и порт сокета другой стороны.
- `State` - состояние сокета.

- `0.0.0.0` - принимать соединение на любом адресе, назначенном системой.

---

# Task Task

## Установи и запусти утилиты top и htop.

- Изначально были установлены, потому просто запустил командами `top` и `htop`

## По выводу команды `top` определено: 

- `uptime` - 2:19
- `количество авторизованных пользователей` - 1
- `среднюю загрузку системы` - 0.02, 0.01, 0.00
- `общее количество процессов` - 92
- `загрузку cpu` - 0.4 us, 0.4 sy, 0.0 ni, 99.1 id, 0.0 wa, 0.0 hi, 0.0 si, 0.0 st
- `загрузку памяти` - 302.5
- `pid процесса занимающего больше всего памяти` - 1840
- `pid процесса, занимающего больше всего процессорного времени` - 1840 

## htop

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/htop_sort_pid.png?ref_type=heads)
- отсортированный по `PID`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/htop_sort_percent_cpu.png?ref_type=heads)
- отсортированный по `PERCENT_CPU`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/htop_sort_percent_mem.png?ref_type=heads)
- отсортированный по `PERCENT_MEM`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/htop_sort_time.png?ref_type=heads)
- отсортированный по `TIME`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/htop_filter_sshd.png?ref_type=heads)
- отфильтрованный для процесса sshd

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/htop_search_syslog.png?ref_type=heads)
- с процессом syslog, найденным, используя поиск

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/htop_add_hostname_clock_uptime.png?ref_type=heads)
- с добавленным выводом hostname, clock и uptime

---

# Task Task

## Запусти команду fdisk -l.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/fdisk-l.png?ref_type=heads)
- вывод команды `fdisk -l`

- название жесткого диска: /dev/sda
- размер: 25 Gib
- количество секторов: 52428800

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/free-h.png?ref_type=heads)
- вывод команды `free -h`

- размер swap: 2 Gi

---

# Task Task

## Запусти команду df.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/df.png?ref_type=heads)
- вывод команды `df`

- размер раздела: 11758760
- размер занятого пространства: 6244264
- размер свободного пространства: 4895388
- процент использования: 57%

- единица измерения в выводе: килобайты

## Запусти команду df -Th.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/df-Th.png?ref_type=heads)
- вывод команды `df -Th`

- размер раздела: 12 Gi
- размер занятого пространства: 6 Gi
- размер свободного пространства: 4.7 Gi
- процент использования: 57%

- тип файловой системы для раздела: ext4

---

# Task Task

## Запусти команду du.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/du.png?ref_type=heads)
- вывод команды `du`

## Выведи размер папок /home, /var, /var/log (в байтах, в человекочитаемом виде).

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/du-sb-home.png?ref_type=heads)
- вывод размера `/home` в байтах

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/du-sh-home.png?ref_type=heads)
- вывод размера `/home` в человекочитаемом формате

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/du-sb-var.png?ref_type=heads)
- вывод размера `/var` в байтах

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/du-sh-var.png?ref_type=heads)
- вывод размера `/var` в человекочитаемом формате

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/du-sb-var-log.png?ref_type=heads)
- вывод размера `/var/log` в байтах

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/du-sh-var-log.png?ref_type=heads)
- вывод размера `/var/log` в человекочитаемом формате

## Выведи размер всего содержимого в /var/log (не общее, а каждого вложенного элемента, используя *).

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/du-var-log.png?ref_type=heads)
- вывод размера содержимого `/var/log` командой `sudo du /var/log/*`

---

# Task Task

## Установи утилиту ncdu.

- проверил обновления командой `sudo apt update`
- использовал команду `sudo apt install ncdu`

## Выведи размер папок /home, /var, /var/log.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/ncdu-home.png?ref_type=heads)
- вид утилиты `ncdu`, запущенной командой `ncdu /home`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/ncdu-var.png?ref_type=heads)
- вид утилиты `ncdu`, запущенной командой `ncdu /var`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/ncdu-var-log.png?ref_type=heads)
- вид утилиты `ncdu`, запущенной командой `ncdu /var/log`

---

# Task Task

## Открой для просмотра:

1. /var/log/dmesg
2. /var/log/syslog
3. /var/log/auth.log

- открыл командами `vim /var/log/dmesg`, `vim /var/log/syslog` и `vim /var/log/auth.log`

## Время последней успешной авторизации, имя пользователя и метод входа в систему.

- открыл логи авторизаций командой `vim /var/log/auth.log`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/authlog.png?ref_type=heads)
- вид файла `auth.log`

- время последней успешной авторизации: 21:47:44
- имя пользователя: aemonhul
- метод входа в систему: локальный вход через виртуальную консоль

## Перезапусти службу SSHd

- использовал команду `sudo systemctl reload ssh.service`
- открыл файл `/var/log/syslog` командой `vim /var/log/syslog`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/sshdreload.png?ref_type=heads)
- логи рестарта службы `sshd`

---

# Task Task

## Используя планировщик заданий, запусти команду uptime через каждые 2 минуты.

- открыл файла для записи задач командой `crontab -e`
- отредактировал файл, добавив в конце `*/2 * * * * uptime`
- выполнил команду `crontab -l`, чтобы вывести список всех задач

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/crontabl.png?ref_type=heads)
- вывод команды `crontab -l`

- открыл логи командой `vim /var/log/syslog`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/syslogcron.png?ref_type=heads)
- запись в логах о выполнении задач планировщиком `cron` 

## Удали все задания из планировщика заданий.

- выполнил удаление всех задач командой `crontab -r`
- посмотрел список задач командой `crontab -l`

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/crontabrl.png?ref_type=heads)
- список задач после удаления





