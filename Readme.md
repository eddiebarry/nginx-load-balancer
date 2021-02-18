container_name=nginx
docker build -t $container_name . && docker run -it --net=host $container_name

docker rm nginx_load_balance
docker build -t nginx_test .
docker run --net=host --name nginx_load_balance nginx_test




# Rebuild
```
docker-compose up --build --force-recreate --no-deps
```