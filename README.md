# docker-getting-started

## How to launch the Docker container:
> docker build -t getting-started . <br />
> docker run -dp 3000:3000 getting- <br />

## To push the instance...
> docker tag getting-started YOUR-USER-NAME/getting-started <br />
> docker push YOUR-USER-NAME/getting-started <br/>

## To make a volume that persists...
> docker volume create todo-db <br/>
> docker run -dp 3000:3000 -v todo-db:etc/todos getting-started <br />

## To run the instance in development mode...
> docker run -dp 3000:3000 -w /app -v "$(pwd):/app" node:12-alpine sh -c "yarn install && yarn run dev"