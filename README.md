<h1 align="center">RefuApp Main Repository ⛰️🏠</h1>

This repository contains all the services you need for running an instance of RefuApp!

## Running Locally 🏠🚀
You can run refuapp locally with docker compose with the following command:

```shell
docker-compose -f docker-compose-local.yml up -d --build
```

## Deploy 🌎💫
You can deploy to our linode server doing push to the main branch of this repo:
```shell
git pull
git submodule update --init --remote --recursive
# Add changed submodules or config files
git push
```
