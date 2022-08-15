# gh-actions-docker-spa

This GitHub Action will build your vite app and turn it into a docker container

Tested with vite

Assumptions (will turn into parameters later):

* docker name is the one of the repo
* docker runs on 3000
* index.html is the entry point
* `yarn` is used
* the build command is `yarn build`
* the result of the build is in `/dist`
* `VITE_VERSION` and `VITE_GIT_SHA` will contain the version and the sha
