```javascript

> docker network create favorites-net
> docker run -d --rm --name mongodb --network favorites-net mongo
> docker build -t favorites-node .
> docker run --name favorites --network favorites-net -d --rm -p 9000:3000 favorites-node
```