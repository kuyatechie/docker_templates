# docker_templates
A collection of Docker templates for creating base images

# Docker base images
Dockerfiles for base images

## Build Steps
Version control: Major release corresponds to the major version release of the source. Minor release corresponds to minor fixes required in the local base image.os.

Docker tag: <original_image_name>:img-<dockerhub_tag>-<img_version_control>

## Dockerfile LABEL templates
Replace all with <> in template

### OS formats
```
## File Created: <dd.mm.yyyy>

ARG REGISTRY

FROM ${REGISTRY:+$REGISTRY/}<base_img>:<tag>

ARG TITLE="<img_name:dockerhub_tag>"
ARG DESCRIPTION="Custom <title> base docker image"
ARG MAINTAINER="<maintainer_name>"
ARG MAINTAINER_EMAIL="<maintainer_email>"
ARG DOCUMENTATION="https://github.com/kuyatechie/docker_templates/blob/main/README.md"
ARG SOURCE="1"
ARG LICENSES="<licensing_url>"

## parameters for builds
ARG BUILD_DATE="dd.mm.yyyy"
ARG VCS_REF="1"
ARG BUILD_VERSION="1"

## input files
ARG <...>

## labels
LABEL org.opencontainers.image.author $MAINTAINER
LABEL org.opencontainers.image.maintainer $MAINTAINER_EMAIL
LABEL org.opencontainers.image.created $BUILD_DATE
LABEL org.opencontainers.image.source $SOURCE
LABEL org.opencontainers.image.version $BUILD_VERSION
LABEL org.opencontainers.image.revision $VCS_REF
LABEL org.opencontainers.image.title $TITLE
LABEL org.opencontainers.image.description $DESCRIPTION
LABEL org.opencontainers.image.documentation $DOCUMENTATION
LABEL org.opencontainers.image.licenses $LICENSES

##################################################################################################
```

### Level formats
```
## File Created: <dd.mm.yyyy>

ARG REGISTRY

FROM ${REGISTRY:+$REGISTRY/}<base_img>:<tag>

ARG IMAGE_NAME="<img_name>"
ARG TITLE="<img_name:dockerhub_tag>"
ARG DESCRIPTION="Custom <title> base docker image"
ARG MAINTAINER="<maintainer_name>"
ARG MAINTAINER_EMAIL="<maintainer_email>"
ARG DOCUMENTATION="https://github.com/kuyatechie/docker_templates/blob/main/README.md"
ARG SOURCE="1"
ARG LICENSES="<licensing_url>"

## parameters for builds
ARG BUILD_DATE="1.1.2021"
ARG VCS_REF="1"
ARG BUILD_VERSION="1"

## input files
ARG <...>

## labels
LABEL org.opencontainers.image.$IMAGE_NAME.author $MAINTAINER
LABEL org.opencontainers.image.$IMAGE_NAME.maintainer $MAINTAINER_EMAIL
LABEL org.opencontainers.image.$IMAGE_NAME.created $BUILD_DATE
LABEL org.opencontainers.image.$IMAGE_NAME.source $SOURCE
LABEL org.opencontainers.image.$IMAGE_NAME.version $BUILD_VERSION
LABEL org.opencontainers.image.$IMAGE_NAME.revision $VCS_REF
LABEL org.opencontainers.image.$IMAGE_NAME.title $TITLE
LABEL org.opencontainers.image.$IMAGE_NAME.description $DESCRIPTION
LABEL org.opencontainers.image.$IMAGE_NAME.documentation $DOCUMENTATION
LABEL org.opencontainers.image.$IMAGE_NAME.licenses $LICENSES

##################################################################################################
```