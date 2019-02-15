# pi hole

This repo contains the docker-compose file I use to bring up the pi-hole container on my network. This config uses the official [pihole docker image](https://hub.docker.com/r/pihole/pihole). 

Check the [docker hub page](https://hub.docker.com/r/pihole/pihole#environment-variables) for more information on settings you can add to the `docker-compose.yml`.

To get this running, simply clone this repo, modify the settings and run: 

```
$ docker-compose up -d
```

## settings

You'll want to open up `docker-compose.yml` and modify the following settings:

* `dns` - This is an array of ips that the container will use for dns lookups
* `environment` - This is a dictionary of keys, you'll want to modify `ServerIP` and set this to the IP of your host. You'll also want to specify `DNS1` and `DNS2`, which pi-hole will use for dns lookups.

