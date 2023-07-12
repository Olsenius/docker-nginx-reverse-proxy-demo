## Docker nginx sample

Start everything with `docker compose up` or `docker compose up -d` for detatched mode. 

This will spin up a MariaDB instance available on `localhost:3306` and `db:3306` from the containers.

It will also create two sample web containers `web1` and `web2` serving the files in `./web1/`  and `./web2/`. 

As a way of making `web1` and `web2` accessible we spin up a `nginx` reverse proxy configured in `nginx.conf`. 

The current config will route any request to `localhost.gullane.no` or `*.localhost.gullane.no` to `web1` (As it is the first one defined in nginx.conf) and any request to `web2.localhost.gullane.no` to `web2`.