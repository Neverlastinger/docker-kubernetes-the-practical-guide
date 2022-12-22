```javascript

> docker build -t mynpm .
> docker run -it -v $(pwd):/app mynpm init
> docker run -it -v $(pwd):/app mynpm install express --save
```
or
```javascript

> docker-compose run --rm npm init
```