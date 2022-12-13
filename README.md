```javascript

> docker build .
> docker build -t [app-name[:tag]] .
> docker build -t [app-name[:tag]] --build-arg DEFAULT_PORT=8000 .
> docker run -p 9000:80 -d --rm [id]
> docker run -p 9000:80 -d --rm --name feedback-app [id]
> docker run -p 9000:80 -d --rm --name feedback-app -v feedback:/app/feedback [id]
> docker run -p 9000:80 -d --rm --name feedback-app -v feedback:/app/feedback -v $(pwd):/app -v /app/node_modules [id]
> docker run -p 9000:8000 --env PORT=8000 -d --rm --name feedback-app -v feedback:/app/feedback -v $(pwd):/app -v /app/node_modules [id]
> docker run -p 9000:8000 --env-file ./.env -d --rm --name feedback-app -v feedback:/app/feedback -v $(pwd):/app -v /app/node_modules [id]
> docker run --rm -it [id]
> docker images
> docker image prune -a
> docker ps -a
> docker rm [name]
> docker rmi [name/id]
> docker volume ls
> docker volume prune
```