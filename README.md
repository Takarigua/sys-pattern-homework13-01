# Домашнее задание к занятию "`Уязвимости и атаки на информационные системы`" - `Марченко Вячеслав Игоревич`

---

### Задание 1

Скачайте и установите виртуальную машину Metasploitable: https://sourceforge.net/projects/metasploitable/.

Это типовая ОС для экспериментов в области информационной безопасности, с которой следует начать при анализе уязвимостей.

Просканируйте эту виртуальную машину, используя nmap.

Попробуйте найти уязвимости, которым подвержена эта виртуальная машина.

Сами уязвимости можно поискать на сайте https://www.exploit-db.com/.

Для этого нужно в поиске ввести название сетевой службы, обнаруженной на атакуемой машине, и выбрать подходящие по версии уязвимости.

Ответьте на следующие вопросы:
- Какие сетевые службы в ней разрешены?
- Какие уязвимости были вами обнаружены? (список со ссылками: достаточно трёх уязвимостей)
Приведите ответ в свободной форме.

### Ответ

1. Список сервисов:

![services](https://github.com/Takarigua/sys-pattern-homework13-01/blob/8792023af11a68ee541f6256364582950e9261a9/img/Task%201-1.png)

2. Уязвимость в vsftpd 2.3.4 (FTP): CVE-2011-2523: Backdoor в vsftpd 2.3.4, позволяющий удалённое выполнение кода. Уязвимость в UnrealIRCd 3.2.8.1 (IRC): CVE-2010-2075: Backdoor в UnrealIRCd, позволяющий удалённое выполнение кода. Уязвимость в Samba 3.0.20 (NetBIOS/SMB): CVE-2007-2447: Уязвимость в Samba, позволяющая удалённое выполнение кода через команду username map script.

---

### Задание 2

Проведите сканирование Metasploitable в режимах SYN, FIN, Xmas, UDP.

Запишите сеансы сканирования в Wireshark.

Ответьте на следующие вопросы:
- Чем отличаются эти режимы сканирования с точки зрения сетевого трафика?
- Как отвечает сервер?
Приведите ответ в свободной форме.

### Ответ
1. SYN-сканирование: Отправляет SYN-пакеты и ожидает SYN-ACK. Если получен SYN-ACK, порт считается открытым.
FIN-сканирование: Отправляет FIN-пакеты. Если порт закрыт, сервер отправляет RST-пакет.
Xmas-сканирование: Отправляет пакеты с флагами FIN, PSH и URG. Если порт закрыт, сервер отправляет RST-пакет.
UDP-сканирование: Отправляет UDP-пакеты. Если порт закрыт, сервер отправляет ICMP-сообщение "Port Unreachable".

```
Поле для вставки кода...
....
....
....
....
```

`При необходимости прикрепитe сюда скриншоты
![Название скриншота 2](ссылка на скриншот 2)`


---

