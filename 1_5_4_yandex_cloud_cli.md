# Практическая работа. Знакомство с Yandex Cloud CLI

Устанавливаем CLI согласно инструкции - https://cloud.yandex.ru/docs/cli/quickstart

Создаем профиль и проверяем консоль:
```bash
# при инициализации вводим токен и базовые настройки
yc init

# проверяем, что консоль работает
yc config list
```

Создаем файл `startup.sh` со следующим содержимым:
```bash
#!/bin/bash
apt-get update
apt-get install -y nginx
service nginx start
sed -i -- "s/nginx/Yandex Cloud - ${HOSTNAME}/" /var/www/html/index.nginx-debian.html
EOF 
```

Создаем первую виртуальную машину:
```bash
yc compute instance create \
    --name demo-1 \
    --hostname demo-1 \
    --metadata-from-file user-data=startup.sh \
    --create-boot-disk image-folder-id=standard-images,image-family=ubuntu-2004-lts \
    --zone ru-central1-a \
    --network-interface subnet-name=default-ru-central1-a,nat-ip-version=ipv4 
```

Создаем вторую виртуальную машину:
```bash
yc compute instance create \
    --name demo-2 \
    --hostname demo-2 \
    --metadata-from-file user-data=startup.sh \
    --create-boot-disk image-folder-id=standard-images,image-family=ubuntu-2004-lts \
    --zone ru-central1-a \
    --network-interface subnet-name=default-ru-central1-a,nat-ip-version=ipv4 
```

Проверяем, что две ВМ создались и запустились:
```bash
yc compute instance list
# +----------------------+------------+---------------+---------+-----------------+-------------+
# |          ID          |    NAME    |    ZONE ID    | STATUS  |   EXTERNAL IP   | INTERNAL IP |
# +----------------------+------------+---------------+---------+-----------------+-------------+
# | fhm6eb8bg5j8l25m5i01 | demo-2     | ru-central1-a | RUNNING | 158.160.112.131 | 10.128.0.32 |
# | fhmr5t3pu3r57tadm4io | demo-1     | ru-central1-a | RUNNING | 158.160.107.5   | 10.128.0.34 |
# +----------------------+------------+---------------+---------+-----------------+-------------+
```