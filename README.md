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
      - uses: nexys-system/gh-actions-docker-spa@v0.0.15
```

## Parameters

* docker name is the one of the repo
* docker runs on port 3000, can be overriden with `port`
* index.html is the entry point, can be overriden with `html-entry`
* `yarn` is used
* the build command is `yarn build`
* the result of the build is in `/dist`, can be overriden with `distFolder`
* `VITE_VERSION` and `VITE_GIT_SHA` will contain the version and the sha


