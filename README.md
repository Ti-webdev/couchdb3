1. add admin username & password to `local.d/admins.ini`
2. run

```sh
docker run -u0 --rm -ti -v $PWD/data:/data ibmcom/couchdb3 chown couchdb. /data && docker run -d -P -v $PWD/data:/opt/couchdb/data -v $PWD/local.d:/opt/couchdb/etc/local.d --name=couch3 --restart=unless-stopped -p 5984:5984 ibmcom/couchdb3
```