DEVOPS: Docker / Wordpress
==========================

Docker compose stack to easily install Wordpress

Installation
------------

First, you need to install docker on your computer: [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/).

Then retrieve the docker compose file shared in this git repository: [https://raw.githubusercontent.com/konandrum/devops-docker-prestashop/main/docker-compose.yaml](https://raw.githubusercontent.com/konandrum/devops-docker-prestashop/main/docker-compose.yaml)

Now you can deploy the docker-compose stack like this:
```sh
$ cd path/to/the/docker-compose-directory
$ docker-compose up -d
```

You should have 2 more containers running on your docker engine.

To check, run the following command:
```sh
$ docker ps
```


How to access the Wordpress web application
-------------------------------------------

As you can see in the docker-compose file, the application is running over the `8070` port.

```yaml
...
  wordrpess_app:
    image: wordpress:php7.4-apache
    ports:
      - '8070:80'
...
```

So simply open a browser, and go to the following url: [http://127.0.0.1:8070](http://127.0.0.1:8070)

You can change the allocated port if this one is already used.