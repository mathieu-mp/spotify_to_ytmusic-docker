# spotify_to_ytmusic-docker
Docker image for spotify_to_ytmusic

* This project allows for running spotify_to_ytmusic from a docker container

## Usage
### Build the image
TODO: doc

### Initial setup via cli
From the docker host:
1. On the docker host, create the voume storage: `mkdir /docker/spotify_to_ytmusic`
1. On the docker host, enter the container: `docker run -it --rm -v /docker/spotify_to_ytmusic:/root/.cache/spotify_to_ytmusic/ spotify_to_ytmusic /bin/sh`
1. In the container, run `spotify_to_ytmusic setup`

### Create usage via cli

1. On the docker host, enter the container: `docker run -it --rm -v /docker/spotify_to_ytmusic:/root/.cache/spotify_to_ytmusic/ spotify_to_ytmusic /bin/sh`
1. In the container, run `spotify_to_ytmusic create <spotify_https_url>`
1. At first launch, spotify_to_ytmusic will require you to complete the OAuth via your browser.

### Update usage via cli

1. On the docker host, enter the container: `docker run -it --rm -v /docker/spotify_to_ytmusic:/root/.cache/spotify_to_ytmusic/ spotify_to_ytmusic /bin/sh`
1. In the container, run `spotify_to_ytmusic update --append APPEND <spotify_https_url> <ytmusic_playlist_name>`

### Update usage via docker-compose
1. Create a `compose.yaml` for your environment, based on the [compose.yaml](compose.yaml) example file
1. Run `docker-compose run --rm spotify_to_ytmusic`

## Requirements
### Software
* Required: Docker
* Required: Docker Compose

The Docker Compose [documentation](https://docs.docker.com/compose/install/)
contains a comprehensive guide explaining several install options. On recent debian-based systems, Docker Compose may be installed by calling
  ```sh
  $ sudo apt install docker-compose
  ```

## References
* This project is an integration of
  * [spotify_to_ytmusic](https://github.com/sigma67/spotify_to_ytmusic)
  * [Docker](https://www.docker.com)