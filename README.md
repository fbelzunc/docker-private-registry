# docker-private-registry
Docker Private Registry with Basic Authentication

## Create the htpasswd_backup

```
# Create the htpasswd_backup
mkdir -p ~/htpasswd_backup
docker run --rm --entrypoint htpasswd registry:2 -Bbn admin "admin" > ~/htpasswd_backup/htpasswd
```

## To launch

```
docker-compose -f docker-compose.yml -f docker-compose.auth.yml up -d
```


The credentils for Basic Authentication are:

```
username: admin
password: admin
```
