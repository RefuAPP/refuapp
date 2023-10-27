<h1 align="center">RefuApp Main Repository ⛰️🏠</h1>

This repository contains all the services you need for running an instance of RefuApp!

## Running Locally 💻🚀

### Configure your Google Maps API key 🔑
By default, all the environment variables are loaded from the [.env file](.env). All the default values have straightforward values, except for the `FRONTEND_MAPS_API_KEY`. This variable should be provided by you, as it is necessary for loading the map on the home page.

To obtain your API key, you can [get it from the Google Cloud page](https://developers.google.com/maps/get-started).

### Running with Docker 🐳
Since our architecture consists of different backend and frontend services behind a proxy, the easiest way to run it locally is with `docker-compose`:

```shell
git clone --recursive git@github.com:RefuAPP/refuapp.git
docker-compose -f docker-compose.yml -f docker-compose.local.yml up -d --build
```

## Deploy 🌎💫
You can deploy to our linode server doing push to the main branch of this repo:
```shell
git pull
git submodule update --init --remote --recursive
# Add changed submodules or config files
git push
```
