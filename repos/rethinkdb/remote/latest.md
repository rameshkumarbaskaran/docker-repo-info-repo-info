## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:3525b9b8277f9056cb1ac4d192c77eb7118e292570847ac965336e21285cde26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:af88cb60c22c03338c3cbb35ee962d411a96ae2d34b55a07e06830a982ee5213
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47932023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5e5887e45c6244aef237c496fcab5a47414fabd9fa47478804c525c6ec1bdb`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 15:25:57 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 15:25:59 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 12 Jul 2022 15:25:59 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 12 Jul 2022 15:26:05 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 15:26:05 GMT
VOLUME [/data]
# Tue, 12 Jul 2022 15:26:05 GMT
WORKDIR /data
# Tue, 12 Jul 2022 15:26:05 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 12 Jul 2022 15:26:05 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0337deed8224ea2e7c0ca5e077c62939d704d7306ada45e847cb504c8c03bf25`  
		Last Modified: Tue, 12 Jul 2022 15:26:20 GMT  
		Size: 6.3 MB (6326840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191a5691db899e2953b0bc2290bf23b2fb61433fd3cca052ae314ec10722c54b`  
		Last Modified: Tue, 12 Jul 2022 15:26:19 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78e81da69a5aa3227e86434456376e58469c15945c381af45fd9e30f012c12f`  
		Last Modified: Tue, 12 Jul 2022 15:26:21 GMT  
		Size: 10.2 MB (10235760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1079a17c34a30028313ceb7f6c634b5c277b3bbcc42095e1d0d381c5569b726`  
		Last Modified: Tue, 12 Jul 2022 15:26:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:17d7c9cde5375503e4d61ff9019b33e6521fe0e59ce921ba96f4c68bf707ba7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45736592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a85a60426b38b58b0447a563ace957c33cd16e38ec2f010be09a69c03be2a1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 12:58:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 12 Jul 2022 12:58:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 12 Jul 2022 12:58:58 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:58 GMT
VOLUME [/data]
# Tue, 12 Jul 2022 12:58:59 GMT
WORKDIR /data
# Tue, 12 Jul 2022 12:59:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 12 Jul 2022 12:59:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd64d21079be01bfbfc2e3c03b980dae2555e3cde8f67989d6548e0a0c4b9e1`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 6.3 MB (6307438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4867547263d5c578be8d148bf9a3b99b196f59f9627d30c077b367aceb822369`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6caa23d65e5714906e1c7785d47a85e8dbff934bdcce0d4c02133f88182274`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 9.4 MB (9372166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f74bd782c64b26192fdef2ea0fce33f70798cf991501e67b01d016173cf896`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:c8408ac4f3bdafe1226456fd16376e591cacbfa8de259923e09b8b35bdb7ca4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45419547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0076cb3120e9226025b2fabd799c363b078af682ccee8922caeaebd70f855399`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 12 Jul 2022 00:43:45 GMT
ADD file:70135711d42f7b2b32586e31afb57a0590019326efa82abf1402dc7a8f02a3f2 in / 
# Tue, 12 Jul 2022 00:43:49 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 16:00:38 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 16:00:41 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 12 Jul 2022 16:00:42 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 12 Jul 2022 16:00:52 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 16:00:54 GMT
VOLUME [/data]
# Tue, 12 Jul 2022 16:00:55 GMT
WORKDIR /data
# Tue, 12 Jul 2022 16:00:55 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 12 Jul 2022 16:00:55 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:447abc12b0c6da6e339b4fa17a2a7dd672d6f0631d30ee44c28b8b06e78884bd`  
		Last Modified: Tue, 12 Jul 2022 00:53:41 GMT  
		Size: 29.6 MB (29640209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143ba62ba31e365491492a3e52c8e2c5eb508e56a67b5fc0830aea56c82c8db2`  
		Last Modified: Tue, 12 Jul 2022 16:01:30 GMT  
		Size: 6.2 MB (6204024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d621e03ff9f857dddbc6c5dc6b43290f998c09b83ce2222e35a93ed8a66650f8`  
		Last Modified: Tue, 12 Jul 2022 16:01:29 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032221f765b1a2edbdbb3f21e3583e9da17a9ecc7da6c60b175a2ef553216cd3`  
		Last Modified: Tue, 12 Jul 2022 16:01:31 GMT  
		Size: 9.6 MB (9572498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a1fd668046da70882ed5cab6092d410282b0930cee27d7d845a294320ca3c4`  
		Last Modified: Tue, 12 Jul 2022 16:01:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
