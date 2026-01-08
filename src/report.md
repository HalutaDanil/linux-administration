# Task 1

## Установи Ubuntu 20.04 Server LTS без графического интерфейса. (Используем программу для виртуализации — VirtualBox)

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/task1.png)

# Task 2

## Создай пользователя, отличного от созданного при установке. Пользователь должен быть добавлен в группу `adm`.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/task2-createuser-and-appendadm.png)

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/task2-passwd.png)

# Task 3

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

# Task 4

## Обнови системные пакеты до последней на момент выполнения задания версии.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/task4.png?ref_type=heads)
- Использование команды `apt update` и команды `apt upgrade`

# Task 5

## Разреши пользователю, созданному в Part 2,выполнять команду sudo.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/task5.png?ref_type=heads)
- Изменение `hostname`, созданным пользователей

- Команда `sudo` дает пользователю временные права суперпользователя для выполнения задач, для доступа к которым нужны административные права.

# Task 6 

## Настрой службу автоматической синхронизации времени.

![](https://git.21-school.ru/students_repo/aemonhul/D01_Linux.ID_356272-1/raw/develop/src/image_for_md/task6.png?ref_type=heads)
- Использование команды `timedatectl` и команды `date`

# Task 7

## Установи текстовые редакторы VIM (+ любые два по желанию NANO, MCEDIT, JOE и т. д.)

- Установил редакторы VIM, NANO, MCEDIT.

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


