# Refuapp main repository 🏠

## Setting up API Keys 🔑

This project uses Google Maps and Google Places services. In order to use those services an API Keys is needed. Since making calls to the Google APIs from the proejct frontend exposes those keys, there is a key for production (whose usage is restricted to this projects domain name) which can be
safely exposed, and a key for development which **must remain secret**.

The production API key sets itself through the CI, but when developing on a local machine the following files have to be modified to include the dev key:

```ts
file: refuapp-frontend/app/src/environment/environment.secret.ts

export const environment = {
  mapsKey: 'DEV_API_KEY',
};
```

```ts
file: refuapp-frontend/app/android/local.properties
MAPS_API_KEY='DEV_API_KEY'
```

```html
file: refuapp-frontend/app/src/index.html

...
<script src="https://maps.googleapis.com/maps/api/js?key='DEV_API_KEY'&libraries=places&language=ca"></script>
```

## Pull the latest changes on all linked repositories 🔀
```shell
git submodule update --init --remote --recursive
```
