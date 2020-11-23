## alpine
### alpine-3.10
Local Version control: 1.0

Docker tag: alpine:img-<alpine_version>-1.0

Builds: https://dl-4.alpinelinux.org/alpine/v3.10/releases/x86_64/

#### Dockerfile Source
1.0 https://github.com/alpinelinux/docker-alpine/blob/da78fcf5c5da55092aa82a97095274b3df648866/x86_64/Dockerfile

#### Prerequisites
##### Docker image requirements
scratch

##### External dependency
No

##### Source tarball
https://dl-4.alpinelinux.org/alpine/$SOURCE_VERSION/releases/x86_64/alpine-minirootfs-3.10.2-x86_64.tar.gz

1.0 https://dl-4.alpinelinux.org/alpine/v3.10/releases/x86_64/alpine-minirootfs-3.10.2-x86_64.tar.gz

#### Command
`docker build --build-arg BUILD_DATE=<sample_date> --build-arg VCS_REF=<sample_ref_id> --build-arg BUILD_VERSION=<sample_ver> --build-arg SOURCE=<source_url> --build-arg --file alpine/alpine-3.10 --tag alpine:img-3.10-1.0 alpine`