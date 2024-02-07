## Run the below commands to host the feed-back app

```
docker build -t feedback-node .

docker run -p 3000:80 -d --name feedback-app --rm feedback-node

Launch in browser http://localhost:3000

```

## Stop the application i.e. stop the container

```
docker stop feedback-app

```
