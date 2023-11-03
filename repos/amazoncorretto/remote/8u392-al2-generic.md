## `amazoncorretto:8u392-al2-generic`

```console
$ docker pull amazoncorretto@sha256:d90382f8d044ce948fc6600296cc54fe83cccc626556a7541691e4173f2aa43a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u392-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:05638b32be6627287da17cc22a84666effdbfffdd0293e1ea72dda024f06e9f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138233342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7269e6fb558689397b0fecb95cde4566468077d5b404380960603f5f6f626402`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:21:53 GMT
COPY dir:3e6cf913ede7c7c09de0465c096dad9a8bea883f026db356d68f0e799e2e3847 in / 
# Fri, 03 Nov 2023 22:21:53 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 22:38:47 GMT
ARG version=1.8.0_392.b08-1
# Fri, 03 Nov 2023 22:39:09 GMT
# ARGS: version=1.8.0_392.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Nov 2023 22:39:09 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 22:39:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:6ebddf7084e9402a3ba6cf1360703e12633f9c49f51772f99c298cd1048d728e`  
		Last Modified: Fri, 03 Nov 2023 11:40:21 GMT  
		Size: 62.6 MB (62646469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e94e63f60b4802fe552c16fdf0857fa14a4d72107a01b9bbd60dc9c1d8b7a2b`  
		Last Modified: Fri, 03 Nov 2023 22:52:21 GMT  
		Size: 75.6 MB (75586873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u392-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c0f386e85785be23e4b475bd2e00bf2dfc43046d4c4472fb18fff988794e4718
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123993301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645cfb18286e6a1465d047c51aeaefaeb3eabbec8ea5b3b9b7f52024f010aecc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:40:19 GMT
COPY dir:fd6882cfe0ef7631745084a3b6ac01566c46fa528d35361defcd296ca1356d38 in / 
# Fri, 03 Nov 2023 22:40:20 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 22:56:15 GMT
ARG version=1.8.0_392.b08-1
# Fri, 03 Nov 2023 22:56:31 GMT
# ARGS: version=1.8.0_392.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Nov 2023 22:56:32 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 22:56:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:615a413db4e82f95ffe4a1cef67468f86d056893cb442e21cb7cea8bc622f9d0`  
		Last Modified: Fri, 03 Nov 2023 17:50:57 GMT  
		Size: 64.4 MB (64380203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5a65a128cd0e4a050ccae0c23b1c346c7b82b679bf029de348d4536709ade2`  
		Last Modified: Fri, 03 Nov 2023 23:06:52 GMT  
		Size: 59.6 MB (59613098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
