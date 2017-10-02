### Commands

##### Setup

    touch Dockerfile app.py requirements.txt

##### Build

    docker build -t friendlyhello .

##### Running

    docker run -p 4000:80 friendlyhello
    docker run -d -p 4000:80 friendlyhello
    docker run -p 4000:80 boycook/getting-started:part2
    curl http://localhost:4000

##### Stack

    docker swarm init
    docker stack deploy -c docker-compose.yml getstartedlab


##### Tag and Deploy

    docker tag friendlyhello boycook/getting-started:part2
    docker push boycook/getting-started:part2

##### Inspect and Teardown

    docker service ls
    docker container ls -q
    docker node ls
    docker stack rm getstartedlab
    docker swarm leave --force
