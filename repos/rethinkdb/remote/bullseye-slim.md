## `rethinkdb:bullseye-slim`

```console
$ docker pull rethinkdb@sha256:eccd36e393e492101f8d61f2fe2b6abca0aefa3c6730b53d23828e4020aadd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:70f6faa59f8b4967db6d28bbe84444c7fe627b03fe1a489b82e58f13b0a8b666
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47964340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acffac2bf53c51984a36f3906662056528df679e3ea208beacf5c287187212a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 13:01:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:01:56 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 13:01:56 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 13:02:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:02:02 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 13:02:02 GMT
WORKDIR /data
# Sat, 04 Feb 2023 13:02:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 13:02:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53fa130c1287ce339095f98c31e66efa9fd01726eb298f6645bff2667c9f7f0`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 6.3 MB (6328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75ff9d0caee22fca325efbb885a0a0a25fbf216384fb1b1fe1bc75e09319d6b`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38873e24b4376c03c1a284f0ba0bc52dced59107fc146c04e44504b678e77d40`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 10.2 MB (10235828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48054ab7bc7eb6d00ba095d1bda52291ae36fef7dfa8da5a0b8a88a6ea7cd932`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:a03b9bb9465a2ebe19f2322431bf274c1c26e330a328a7dfa2e17dffc2385cf3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45944921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168a189f7011ca6f003ea49717e21ae698d3950dee0281e8a0729222100b875d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:21:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:51 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 17:21:51 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 17:21:56 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:56 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 17:21:56 GMT
WORKDIR /data
# Sat, 04 Feb 2023 17:21:56 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 17:21:56 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d38dd4390268ea82788f4098c01533d8c4288e51254613dc8a7c269092d6be5`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 6.3 MB (6309522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f40f152e66346a5e4c31f57e37f58cdb7eadbd06d3a5689406ed0671da805c`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b7c10637f23d56c21cc1ab7e09007f63ff491a20e0b96e1595abbaf278b5c`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 9.6 MB (9587793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858cd5a01bebdd3edc1105d92f7126fdf29a90b40efac1f106027b5e919a7e7f`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:1567a44f73035de2de947502fc8224261a375ab8c79a63c0fc85a4211e345de6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45410584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12267b01c5b6c39e19ffcdd7e5d76921f2cb0a0fe4e80c777398e700861fa286`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 04:06:15 GMT
ADD file:29a3ecb38611dbbb6f45b2d10ad3cee60c0198429376f999e9a397f9c405820e in / 
# Sat, 04 Feb 2023 04:06:17 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:47:13 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:47:15 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 10:47:16 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 10:47:40 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:47:41 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 10:47:42 GMT
WORKDIR /data
# Sat, 04 Feb 2023 10:47:43 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 10:47:43 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7c6fe4d1ef15da79055e0a71952e1a38f799d4f36e9acebdb1ec1512651b39f1`  
		Last Modified: Sat, 04 Feb 2023 04:10:27 GMT  
		Size: 29.6 MB (29629678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e5e72ee4c59c1fc0c1d59c59af193c4439d9df9996ede4495bc6394f0f6af4`  
		Last Modified: Sat, 04 Feb 2023 10:48:09 GMT  
		Size: 6.2 MB (6205602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d836436dbcf9d9f4399b2af6e84652810d276716d7d98eb0845e4fb20f5bca`  
		Last Modified: Sat, 04 Feb 2023 10:48:08 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1764374150ce8e8f40aa48ec1fafe22c89a1a8e9cc3227dada8f6cc58edbb193`  
		Last Modified: Sat, 04 Feb 2023 10:48:10 GMT  
		Size: 9.6 MB (9572491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8911a3baa2d75738a19fde86281776ceed51fbaee06e87ec0fda3f76928390`  
		Last Modified: Sat, 04 Feb 2023 10:48:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
