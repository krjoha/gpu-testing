# gpu-testing


``` bash
docker build -t gpu-testing --build-arg USER_ID=$(id -u) --build-arg GROUP_ID=$(id -g) -f Dockerfile .
docker run -d --rm -it --gpus all --volume $(pwd):/home/jovyan/work --name gpu-testing gpu-testing
docker exec -it gpu-testing /bin/bash
```