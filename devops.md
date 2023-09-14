# DevOps

### Docker commands

- Build:
  ```
  docker build .
  docker build . -t <file-name>
  docker build . --tag <username>/<repository-name>:<version>
  docker compose -f <docker-compose.yml> up build
  ```

- Start: `docker start <container-id|container-name>`
- Run:
  ```
  docker run <image-name>
  docker run -d --name <container-name> <image-name>
  docker run -p 3000:3000 -d --name <container-name> <image-name>
  docker run -p 3000:3000 -v $(pwd):/app -d --name <container-name> <image-name>
  docker run -p 3000:3000 -v $(pwd):/app -v /app/node_modules -d --name <container-name> <image-name>
  docker run -p 3000:3000 -v $(pwd):/app:ro -v /app/node_modules -d --name <container-name> <image-name>
  docker run --env PORT=4000 -p 3000:4000 -v $(pwd):/app:ro -v /app/node_modules -d --name <container-name> <image-name>
  docker run --env-file ./.env -p 3000:4000 -v $(pwd):/app:ro -v /app/node_modules -d --name <container-name> <image-name>
  docker run --name <container-name> \
		-p <port>:<port> \
		-v jenkins_home_3:/var/jenkins_home \
		-v jenkins_backup_3:/srv/backup \
		<username>/<repository-name>:<version>
  ```
- Up:
  ```
  docker compose up
  docker compose up -d
  docker compose up -d --build
  docker compose -f <docker-compose.yml> up -d
  docker compose -f <docker-compose.yml> up -d --build
  docker compose -f <docker-compose.yml> up -d --build -V
  docker compose -f <docker-compose.yml> up -d --build <service-name> --no-deps
  docker compose -f <docker-compose.yml> up -d --force-recreate <service-name> --no-deps
  docker compose -f <docker-compose.yml> up -d <service-name>
  docker compose -f <docker-compose.yml> up -d <service-name> --node-deps
  docker compose -f <docker-compose.yml> up -d --scale <service-name>=2
  ```

- Down:
  ```
  docker stop <container-id|container-name>
  docker compose down
  docker compose down -v
  docker compose -f <docker-compose.yml> down
  docker compose -f <docker-compose.yml> down -v
  docker swarm leave -f
  ```

- Exec:
  ```
  docker exec -it <service-name> <function>
  docker exec <service-name> <function>
  docker compose exec <service-name> <function>
  ```
- Logs:
  ```
  docker logs <container-id|container-name>
  docker logs <container-id|container-name> -f
  docker compose logs <service-name>
  docker compose logs <service-name> -f
  ```
- Inspect: `docker inspect <container-name> | grep backup`

- Image list: `docker images`
- Container list:
  ```
  docker ps
  docker ps -a
  docker container ps
  docker container ps -a
  ```
- Volume list: `docker volume ls`

- Remove container:
  ```
  docker rm <container-id|container-name>
  docker rm <container-id|container-name> -f
  docker rm <container-id|container-name> -fv
  ```
- Remove image: `docker rmi <image-id|image-name>`
- Remove volume:
  ```
  docker system prune
  docker volume rm <volume-id>
  ```

- Login: `docker login <username>`
- Push: `docker push <username>/<repository-name>:<version>`
