# Облачная система резервного копирования

## Описание
Облачная система резервного копирования для малого бизнеса. Автоматическое создание резервных копий данных пользователей и их хранение в облаке.

## IP адреса нод

| Node name | Hostname           | EXT IP       | INT IP     |
|-----------|--------------------|--------------|------------|
| backup1   | backup1.cloud.org  | 192.168.10.2 | 10.0.0.2   |
| backup2   | backup2.cloud.org  | 192.168.10.3 | 10.0.0.3   |
| storage1  | storage1.cloud.org | 192.168.10.4 | 10.0.0.4   |

## Роли серверов
![тестовое изображение](https://github.com/mzubarik/rebrain-devops-task1/blob/main/images/Logo/Belarus.jpg)

- **Backup(n)**: Серверы для резервного копирования. Управляют процессом создания резервных копий и их восстановлением.
- **Storage(n)**: Серверы хранения данных. Обеспечивают долговременное хранение резервных копий.

## Управление сервисами

### Сервисы :

- Docker
- Restic
- Cron

### Сервисы на storage1:

- Docker
- MinIO

## Установка и настройка
1. Настройка Docker на всех серверах:
   ```bash
   sudo apt-get update
   sudo apt-get install -y docker.io
