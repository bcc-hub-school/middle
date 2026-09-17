# BCC Hub School · Middle

Учебные задания курсов программы Middle.

## Linux Deep

Короткие задания к занятиям (5–10 минут): практика базовых команд и понятий. Один файл на модуль, номер задания = номер занятия.

| Файл | Модуль | Задания |
|---|---|---|
| [`linux-deep/module_1.sh`](linux-deep/module_1.sh) | 1. Linux Fundamentals | `task_1` FHS · `task_2` пользователи, права, ACL, sudo · `task_3` apt и dpkg |
| [`linux-deep/module_2.sh`](linux-deep/module_2.sh) | 2. Process & System Control | `task_4` процессы и сигналы · `task_5` systemd-юниты · `task_6` cron и timers |
| [`linux-deep/module_3.sh`](linux-deep/module_3.sh) | 3. Logging & Observability Basics | `task_7` journald · `task_8` logrotate |

> Запускать **только на учебной ВМ** (Ubuntu 24.04): стенд создаёт и удаляет пользователей, файлы и пакеты.
> Модули 2–3 требуют systemd — нужна обычная ВМ, не контейнер.
> Перед запуском под root скрипт можно и нужно прочитать.

```bash
curl -fsSLO https://raw.githubusercontent.com/bcc-hub-school/middle/main/linux-deep/module_1.sh
# или: wget https://raw.githubusercontent.com/bcc-hub-school/middle/main/linux-deep/module_1.sh

bash module_1.sh list                # какие задания есть
sudo bash module_1.sh setup task_1   # подготовить стенд и показать задание
sudo bash module_1.sh check task_1   # проверить: [ OK ] / [FAIL] и ИТОГ
sudo bash module_1.sh reset task_1   # начать заново
bash module_1.sh task task_1         # ещё раз показать текст задания
```

Для других модулей — то же самое с `module_2.sh` (`task_4`…`task_6`), `module_3.sh` (`task_7`, `task_8`).
