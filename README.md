# rebrain-devops-task1
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
![тестовое изображение] (https://www.google.com/search?q=%D0%B1%D0%B5%D0%BB%D0%B0%D1%80%D1%83%D1%81%D1%8C&sca_esv=56e49c2907496e9a&sca_upv=1&rlz=1C5CHFA_enPL1077PL1077&udm=2&biw=1554&bih=798&sxsrf=ADLYWIJN7eEP0pApG9aIxsMuNwh9c1aXDA%3A1716724397051&ei=rSJTZujmAuuwwPAPt_GbmAg&ved=0ahUKEwio8fPeoKuGAxVrGBAIHbf4BoMQ4dUDCBA&uact=5&oq=%D0%B1%D0%B5%D0%BB%D0%B0%D1%80%D1%83%D1%81%D1%8C&gs_lp=Egxnd3Mtd2l6LXNlcnAiENCx0LXQu9Cw0YDRg9GB0YwyBRAAGIAEMgUQABiABDIFEAAYgAQyBRAAGIAEMgUQABiABDIFEAAYgAQyBRAAGIAEMgUQABiABDIFEAAYgAQyBRAAGIAESLIOUABYrApwAHgAkAEAmAGJAaABhgiqAQMwLji4AQPIAQD4AQGYAgigArAIwgIEECMYJ8ICChAAGIAEGEMYigWYAwCSBwMwLjigB98s&sclient=gws-wiz-serp#vhid=LcJeRCCDLzp9PM&vssid=mosaic)

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