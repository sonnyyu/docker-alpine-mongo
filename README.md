docker build -t docker-mongo .

docker run -d --name docker-mongo -p 27017:27017 -v $(pwd)/data/data:/data/db docker-mongo

To use the mongo shell client:

docker exec -ti docker-mongo mongo

show databases

To run a shell session:

$ docker exec -ti docker-mongo  sh

To clean all docker:

docker container prune -f

docker image prune -a -f

docker volume prune -f

docker network prune -f

docker system prune -f

sudo rm -rf /var/lib/docker/volumes/*
