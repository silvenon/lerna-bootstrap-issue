# Lerna Bootstrap Issue

This repository reproduces issues with `lerna bootstrap` described in https://github.com/lerna/lerna/issues/1457#issuecomment-399678173.

Setup:

```sh
$ git clone https://github.com/silvenon/lerna-bootstrap-issue
$ cd lerna-bootstrap-issue
$ git submodule update --init
$ docker build -t lerna-bootstrap-issue .
```

Run failing script (using `lerna bootstrap`):

```sh
$ docker run --rm lerna-bootstrap-issue scripts/successful
```

Run successful script (using `lerna exec yarn`):

```sh
$ docker run --rm lerna-bootstrap-issue scripts/successful
```

If you want to open a shell session in the Docker container, run:

```sh
$ docker run --rm -ti lerna-bootstrap-issue bash
```
