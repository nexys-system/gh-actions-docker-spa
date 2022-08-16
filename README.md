# gh-actions-docker-spa

This GitHub Action will build your vite app and turn it into a docker container

Tested with vite

see [gh-actions-spa-test](https://github.com/nexys-system/gh-actions-spa-test) if you only need build + test

## Usage

```
name: Docker

on:
  push:
    tags:
      - v*

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: nexys-system/gh-actions-docker-spa@v0.0.19
```

## Parameters

* `container-name`: docker name. Default: name of the repo
* `port`: docker port. Default: `3000`
* `html-entry`: the entry point. Default: `index.html`
* `build-command`: build command. Default is `VITE_VERSION=${GITHUB_REF##*/} VITE_GIT_SHA=$GITHUB_SHA yarn build`
* `distFolder`: folder with the result of the build. Default:`/dist`
* `yarn` is used, to install and test (`yarn test`)
