# wordpress-docker

A simple docker container with mariadb + wordpress

```
$ docker-compose up -d
```

visit http://127.0.0.1:8080

# Come eseguire un backup di un volume su un file

```
docker run --rm
    -v NOME_VOLUME:/backup-volume
    -v CARTELLA_OUTPUT:/backup
    busybox
    tar -zcvf /backup/NOMEFILE /backup-volume
```

esempio:

```
docker run --rm
    -v wordpress_db:/backup-volume
    -v /home/h4shell/:/backup
    busybox
    tar -zcvf /backup/my-backup.tar.gz /backup-volume

```
