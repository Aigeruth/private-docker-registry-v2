# Private Docker distribution (Docker-Registry v2)

This repositry contains a sample production-ready configuration of
Docker-Registry v2 for small teams.

## Configuration

* listens on `5000` port,
* runs as `deploy` user,
* uses filesystem as storage backend,
* stores images under `/data`,
* uses in-memory layer information cache,
* uses [data container pattern](https://docs.docker.com/userguide/dockervolumes/#creating-and-mounting-a-data-volume-container)

## Usage

Start Registry in the background:

```sh
docker-compose up -d
```

## Updating the Docker-Registry version

Remove the `registry` service:

```sh
docker-compose rm registry
```

Update the repository and rebuild the `registry` service:

```
git pull origin master
docker-compose build registry
```
