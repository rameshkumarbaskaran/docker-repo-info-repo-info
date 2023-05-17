## `buildpack-deps:mantic`

```console
$ docker pull buildpack-deps@sha256:eee1fc52e21f774d2621b41092dd31959612de45f7cb7f35dccb3beb5ad90daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	linux; s390x

### `buildpack-deps:mantic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1a1b6f22043a14e5f21097ada8ee77da7fd1720a5f6b87756bee7ccd8ac4f66d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258634583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa51fd3f0a301908b5809ed494b4a3076113c32b878d35c67de912958a12ea89`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 May 2023 12:45:45 GMT
ARG RELEASE
# Tue, 09 May 2023 12:45:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 May 2023 12:45:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 May 2023 12:45:45 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 09 May 2023 12:45:53 GMT
ADD file:87293581d53f522106a37eee2d3056cd4d9bdbb4a58077389c817bd655a4e0c7 in / 
# Tue, 09 May 2023 12:45:53 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:53:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:54:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:55:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e685e76ac424b804c8b8208c603584b34300a955516eaff83d30f060189f522b`  
		Last Modified: Tue, 16 May 2023 23:59:49 GMT  
		Size: 27.0 MB (27026748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccd2979a9c21a4b382153460cb77e2f6d383b4c4cb5cdeb37baa35c84e174a1`  
		Last Modified: Tue, 16 May 2023 23:59:46 GMT  
		Size: 13.4 MB (13350711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342807f1db024cabeca1aa775473201ce240f01d11faabb59c89f443a7bc8cad`  
		Last Modified: Wed, 17 May 2023 00:00:03 GMT  
		Size: 44.1 MB (44062441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8ab9040116d37ac8333ad2979c65a7a380f118dc8791bbcb3ffe9f8f677b7d`  
		Last Modified: Wed, 17 May 2023 00:00:38 GMT  
		Size: 174.2 MB (174194683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:33da28bdfcdfeb866b1146d4bec75d304684df0c7ec98a9cdd4bac2bf21b7ee0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.7 MB (240687349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687e96e9d8cbcc53d6485ce2b68fb535571160c69b06ab7029e1f70d86850a0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 May 2023 13:09:19 GMT
ARG RELEASE
# Tue, 09 May 2023 13:09:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 May 2023 13:09:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 May 2023 13:09:19 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 09 May 2023 13:09:21 GMT
ADD file:a5ed2ab846477e26003abb09795ef405e1d96bec9be1a3cb0b258dd5aa83f075 in / 
# Tue, 09 May 2023 13:09:21 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:52:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:52:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:53:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e21501268ba0e8cdc7e0134b231643691b6d4648511a6bbed295eeca807810d8`  
		Last Modified: Tue, 16 May 2023 23:58:10 GMT  
		Size: 26.2 MB (26239447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b45801daded85936f7c762c0148a3d71e35c237bfe96ba49811f0964c16cb9`  
		Last Modified: Tue, 16 May 2023 23:58:08 GMT  
		Size: 14.0 MB (14018228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1711be48a0a429b31d94131f11f34c0b5f5eb3de15640bbda8ad0c25bba80a0`  
		Last Modified: Tue, 16 May 2023 23:58:21 GMT  
		Size: 44.1 MB (44093858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1c2fdf64d346bbad12a5200032f3bb6be537c79a83306d908f008867fc106c`  
		Last Modified: Tue, 16 May 2023 23:58:45 GMT  
		Size: 156.3 MB (156335816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
