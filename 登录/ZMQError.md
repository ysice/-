1.检查/etc/goodrain/docker-compose.yaml中的console配置

```
console:
  container_name: console
  environment:
  - REGION_TAG=cloudbang
  - MEMCACHED_HOST=127.0.0.1
  - MEMCACHED_PORT=11211
  image: hub.goodrain.com/dc-deploy/console:2017.03
  log_driver: json-file
  log_opt:
    max-size: 50m
  ports:
  - 0.0.0.0:7070:7070
  restart: always
  volumes:
  - /etc/goodrain/console.py:/etc/goodrain/console.py
  - /grdata/services/console:/data
```

2. sed -i 's/zmq_handler/file_handler/' /etc/goodrain/console.py && dc-compose restart console
