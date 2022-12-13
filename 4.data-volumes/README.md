```
> docker build -t feedback-node:final .
> docker run -d -p 9000:80 --rm --name feedback-app -v feedback:/app/feedback -v $(pwd):/app -v /app/node_modules feedback-node:final
> docker run -d -p 9000:8000 --env-file ./.env --rm --name feedback-app -v feedback:/app/feedback -v $(pwd):/app -v /app/node_modules feedback-node:final
```