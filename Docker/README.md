## Manage Data
# create volume
docker volume create mongo_data

docker container create --name mongo -p 27017:27017 -v mongo_data:/data/db mongo:4-xenial

# bind mounts (local storage laptop kita)
docker container create --name mongo -p 27017:27017 -v /users/iqbal/desktop/mongodb:/data/db mongo:4-xenial

#docker exec
docker exec -t -i container_name bin/bash

# Redis
type redis-cli

## membersihkan sampah
docker system df

docker system prune
docker system prune -a --volumes