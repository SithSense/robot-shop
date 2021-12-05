# Microservice Application Output

![Final Screenshot](https://github.com/SithSense/robot-shop/blob/master/web/static/media/stan_robot-shop_final.png)

## Run Locally

Pulled down the images first using:

```shell
$ docker-compose pull
```

Fire up Stan's Robot Shop with:

```shell
$ docker-compose up
```

![docker-compose_up](https://github.com/SithSense/robot-shop/blob/master/web/static/media/docker-compose_pull.png)

## Accessing the Store
Running the store locally via *docker-compose up* then, the store front is available on localhost port 8080 [http://localhost:8080](http://localhost:8080/)

## Changing the logo and updating the main page html.
```shell
$ docker cp web/static/media/cycode_logo.png 5b87afb17366:/usr/share/nginx/html/media/cycode_logo.png
```
```shell
$ docker cp web/static/index.html 5b87afb17366:/usr/share/nginx/html
```

## Merging to master
Some reasons why merging directly to master is not recommended:
* Feature tracking
* Avoid conflicts and potentially broken master. 
* Avoid complexity of isolating features and bugs. 

These may not be top of mind when you are the only developer but I ended up pushing changes to my local branch *John* before merging to master.
```shell
$ git checkout master
$ git pull origin master
$ git merge John
$ git push origin master
```
