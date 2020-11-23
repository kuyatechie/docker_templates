## python
### python-2.7-alpine
Local Version control: 1.0

Docker tag: python:img-<python_version>-1.0

Builds: https://www.python.org/ftp/python/

#### Dockerfile Source
1.0 https://github.com/docker-library/python/blob/aba58b3895e9f50a1323623c18ebe7c969245abc/2.7/alpine3.10/Dockerfile

#### Prerequisites
##### Docker image requirements
alpine:img-3.10-x.x

##### External dependency
Yes

##### Source tarball
https://www.python.org/ftp/python/$PYTHON_VERSION/Python-$PYTHON_VERSION.tar.xz

1.0 https://www.python.org/ftp/python/2.7.16/Python-2.7.16.tar.xz

#### Command
`docker build --build-arg BUILD_DATE=<sample_date> --build-arg VCS_REF=<sample_ref_id> --build-arg BUILD_VERSION=<sample_ver> --build-arg SOURCE=<source_url> --build-arg REGISTRY=<registry> --file python/python-2.7-alpine --tag python:img-2.7-alpine-1.0 python`