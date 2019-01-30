Owncloud in a docker container
=============================

Run the standard owncloud docker image behind a traefik proxy. Traefik will handle https and the certificates. Internally,
the communication runs over simple http.

We are using the standard support images for
- mariadb
- redis
- adminer

The owncloud instance runs on

    oc.example.com/owncloud

and not on the root of the web server.

We provide adminer, but only start it when needed. Use

    ./startup.sh

for normal startup instead of 

    docker-compose up -d

to make sure you only start the required containers, excluding adminer.

