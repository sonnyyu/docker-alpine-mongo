docker build -t docker-mongo .

http://10.145.89.1/

docker run -d --name docker-mongo -p 27017:27017 \
  -v $(pwd)/data/data:/data/db \
  docker-mongo

docker container prune -f

docker image prune -a -f

docker volume prune -f

docker network prune -f

docker system prune -f

sudo rm -rf /var/lib/docker/volumes/*
