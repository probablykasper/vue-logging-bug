# Developper guide

1. Make sure Docker and docker-compose is installed
2. Run `docker-compose run web`
3. open [http://localhost:3000/](http://localhost:3000/)


# Deployment guide

```shell
docker-compose -f docker-compose.prod.yml up --build -d
```
