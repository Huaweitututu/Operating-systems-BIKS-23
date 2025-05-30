# WORK-CASE №7
## 1. Основні функції планувальника задач
### Планувальник задач — це системна служба або утиліта, що дозволяє автоматизувати виконання скриптів, програм або команд у визначений час або інтервал.
#### Основні функції:
- Планування на основі часу (щодня, щогодини, раз на тиждень тощо)
- Повторюваність або одноразовість
- Подієве виконання (наприклад, при запуску системи)
- Логування виконання
- Пріоритезація задач


## 1.1 Порівняння: Linux (Cron) vs Windows (Task Scheduler)
| Ознака                      | Linux (`cron`)                | Windows Task Scheduler                     |
| --------------------------- | ----------------------------- | ------------------------------------------ |
| Графічний інтерфейс         | Ні (CLI)                      | Так                                        |
| Гнучкість форматування часу | Висока (через `crontab`)      | Висока (через GUI або XML)                 |
| Події запуску               | Так (через `cron`, `@reboot`) | Так (часові події, вхід користувача, інші) |
| Повторення                  | Так                           | Так                                        |
| Логування                   | Через syslog / окремі файли   | Через Event Viewer                         |
| Альтернативи                | Так (Anacron, systemd timers) | Можна через PowerShell, Taskschd API       |


#### Cron: принципи роботи та налаштування

cron — демон, що зчитує завдання з crontab файлів і виконує їх у заданий час.
Синтаксис crontab:
![Image](https://github.com/user-attachments/assets/84f6c6c4-0f0d-42a8-9fe7-10cb6b3dc6f6)

#### Приклади:
- Відкрити редактор: crontab -e
- Переглянути список: crontab -l

## Альтернативи до Cron:
| Альтернатива       | Характеристика                                                                                                                |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
| **Anacron**        | Для задач, що не вимагають точного часу, але мають виконуватися щодня/щомісяця навіть при виключеній системі.                 |
| **systemd timers** | Сучасна альтернатива cron для систем з `systemd`. Гнучке керування, інтеграція з `journalctl`, таймери замість `cron`-файлів. |
| **at / batch**     | Виконання одноразових задач у майбутньому.                                                                                    |

# 2. Планування задач

![Image](https://github.com/user-attachments/assets/662c24cb-0879-454d-95b5-13dc380a3ca1)

![Image](https://github.com/user-attachments/assets/6e118595-a73a-4818-8bd1-70275f31e8c0)


# 3. Встановлення та використання альтернативного планувальника задач (systemd Timers) замість Cron 

![Image](https://github.com/user-attachments/assets/cc8010c2-f38d-4abe-9dec-753ec5aaf822)

![Image](https://github.com/user-attachments/assets/e30acfb9-7093-43d4-a635-60ba5164ae77)

![Image](https://github.com/user-attachments/assets/c2b068de-8fa7-4eef-a99e-84d0474beb9f)

![Image](https://github.com/user-attachments/assets/5f057b09-18ea-4cb9-96f5-8d9ed347392a)

![Image](https://github.com/user-attachments/assets/a9313849-384c-493d-bdd6-447a9b98aa53)

![Image](https://github.com/user-attachments/assets/bc6e0ba9-82a3-4b8d-be5b-45380a84545c)

![Image](https://github.com/user-attachments/assets/ff5401b0-8701-496b-9f53-b07c5d7a63d4)

![Image](https://github.com/user-attachments/assets/7ddca4e7-c7ba-4f4f-a6fa-29f8b3489071)
