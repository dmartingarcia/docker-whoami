# docker-homeautomation

It is part of a [set of repositories](https://github.com/search?q=user%3Admartingarcia+docker) that contain dockerised environments for small applications.

In this case, it contains a self-efficient *whoami* setup, that returns your request details, it serves as a test application for connectivity.

## How to use it

```
cp .env.example .env
docker-compose up -d
```

And browse into `http://localhost:8888 in order to see `whoai` response.

After that, you can also set your first sensor using any ESP-8266 / ESP32 compatible device and ESPHome, and connect it to your homeassistant setup.

## Traefik integration`

It also contains a Traefik integration, that interact with this reverse proxy, routing request to each container in case it matches the specified domain

There's a subdomain exposed:
  - whoamiyour.domain.com

## .env setup

It contains a basic set of variables like:

- http host that uses Traefik to match requests

Please take a look on that and :warning: create your own credentials :warning: in case you want to expose it to the public.

## Docker Traefik

If you want to use this Traefik integration, [take a look at this repository](https://github.com/dmartingarcia/docker-traefik)
