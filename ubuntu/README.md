## ubuntu
### ubuntu-xenial
Local Version control: 1.0

Docker tag: ubuntu:img-<ubuntu_version>-1.0

Builds: https://partner-images.canonical.com/core/xenial/

#### Dockerfile Source
1.0 https://github.com/tianon/docker-brew-ubuntu-core/blob/30f325d6526a6dd5ff9f5663a80dcc56db363e2a/xenial/Dockerfile

#### Prerequisites
##### Docker image requirements
scratch

##### External dependency
No

##### Source tarball
https://partner-images.canonical.com/core/xenial/$SOURCE_BUILD_DATE/ubuntu-xenial-core-cloudimg-amd64-root.tar.gz

1.0 https://partner-images.canonical.com/core/xenial/20191010/ubuntu-xenial-core-cloudimg-amd64-root.tar.gz

#### Command
`docker build --build-arg BUILD_DATE=<sample_date> --build-arg VCS_REF=<sample_ref_id> --build-arg BUILD_VERSION=<sample_ver> --build-arg SOURCE=<source_url> --file ubuntu/ubuntu-xenial --tag ubuntu:img-xenial-1.0 ubuntu`