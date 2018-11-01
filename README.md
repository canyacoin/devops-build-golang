# gcloud-golang-111

Cook a build container for GAE projects (with support for Go 1.11 runtime), for use in CI's and local builds

## Create a new Docker image

#### Prerequesites

- [Docker](https://docs.docker.com/install/#releases)

#### Build

```
docker build . -t registry.gitlab.com/canya-com/devops/gcloud-golang-111:X.X # <----- set the tag version plus one
```

Take note of the built imageID

#### Push

```
docker push registry.gitlab.com/canya-com/devops/gcloud-golang-111:X.X <----- set the tag version from the squash step
```

## Running locally

```
docker run -it --entrypoint /bin/bash <imageID>
```

docker push registry.gitlab.com/canya-com/devops/gcloud-golang-111:X.X