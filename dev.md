
### DB and S3
```shell
docker  run --rm --name minio -p 9000:9000 -p 9001:9001   quay.io/minio/minio server /tmp/data --console-address ":9001"

docker run  --rm  --name postgresql \
-p 5432:5432 \
-e POSTGRESQL_USERNAME=root \
-e POSTGRESQL_PASSWORD=password123 \
-e POSTGRESQL_DATABASE=gitea \
bitnami/postgresql:latest
```

### config

```shell
GITEA_APP_INI=/home/lv/lvsoso/gitea/dev-env/app.ini
GITEA_CUSTOM=/home/lv/lvsoso/gitea/dev-env/gitea
GITEA_WORK_DIR=/home/lv/lvsoso/gitea/dev-env/
GITEA_TEMP=/tmp/gitea
GITEA_ADMIN_USERNAME=gitea_admin
GITEA_ADMIN_PASSWORD=abcdefg
```

### Run
```shell
./gitea web -c /home/lv/lvsoso/gitea/dev-env/app.ini
```