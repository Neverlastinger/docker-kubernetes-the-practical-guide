```javascript

> docker network create goals-net
> docker run --name mongodb -v data:/data/db --rm -d --network goals-net -e MONGO_INITDB_ROOT_USERNAME=max -e MONGO_INITDB_ROOT_PASSWORD=secret mongo
> docker build -t goals-node .
> docker run --name goals-backend -v $(pwd):/app -v logs:/app/logs -v /app/node_modules -e MONGODB_USERNAME=max --rm -d --net goals-net -p 80:80 goals-node
> docker build -t goals-react .
> docker run -v $(pwd)/src:/app/src --name goals-frontend --rm -d -p 9000:3000 -it goals-react
```