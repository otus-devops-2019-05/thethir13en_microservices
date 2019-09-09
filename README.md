# thethir13en_microservices
thethir13en microservices repository

## Homework Docker-3

- Переписаны Dockerfiles, уменьшен размер засчет использования Alpine Linux, очистки кеша пакетного менеджера, удаления пакетов необходимых для сборки зависимостей

- Оптимизированы шаги сборки для более оптимального использования кеша

- Исправлены зависимости для Ruby-сервисов, запускаемых в Alpine Linux (отсутствовал gem json)

- Исправлены зависимости для Python-сервиса (отсутствовали пакеты, необходимые для сборки зависимостей)
