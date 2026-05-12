<div align="center">

# Linux Administration

**[English](#english) | [Русский](#русский)**

</div>

---

<a name="english"></a>
## 🇬🇧 English

Fundamental Linux administration skills on Ubuntu Server. Covers installation, user management, network configuration, and working with text editors.

### 🛠️ Tech Stack

![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) ![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=flat-square&logo=ubuntu&logoColor=white) ![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnu-bash&logoColor=white)

### ✨ Features

| Topic | Skills |
|-------|--------|
| Installation | Ubuntu Server LTS without GUI |
| Users | Creation, groups (adm, sudo) |
| Network | Static IP, DNS, DHCP via netplan |
| Time | Timezone, NTP synchronization |
| Packages | apt update/upgrade |
| Editors | VIM, nano, mcedit |
| Monitoring | htop, df, du, free |

### 🚀 Quick Start

```bash
# Create user and add to sudo group
sudo adduser newuser
sudo usermod -aG sudo newuser

# Network configuration
sudo netplan apply

# Check disk usage
df -Th
du -sh /var/log
```

---

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=0:58a6ff,50:1f6feb,100:0969da&height=2&section=header&text=&fontSize=1"/>
</div>

<a name="русский"></a>
## 🇷🇺 Русский

Фундаментальные навыки администрирования Linux на Ubuntu Server. Установка, управление пользователями, сетевая конфигурация, работа с текстовыми редакторами.

### 🛠️ Стек технологий

![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) ![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=flat-square&logo=ubuntu&logoColor=white) ![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnu-bash&logoColor=white)

### ✨ Возможности

| Тема | Навыки |
|------|--------|
| Установка | Ubuntu Server LTS без GUI |
| Пользователи | Создание, группы (adm, sudo) |
| Сеть | Статический IP, DNS, DHCP через netplan |
| Время | Часовой пояс, синхронизация NTP |
| Пакеты | apt update/upgrade |
| Редакторы | VIM, nano, mcedit |
| Мониторинг | htop, df, du, free |

### 🚀 Быстрый старт

```bash
# Создание пользователя и добавление в sudo
sudo adduser newuser
sudo usermod -aG sudo newuser

# Настройка сети
sudo netplan apply

# Проверка использования диска
df -Th
du -sh /var/log
```

---

<div align="center">

*Project from portfolio | Проект из портфолио*

</div>
