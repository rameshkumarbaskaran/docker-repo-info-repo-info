## `rethinkdb:bullseye-slim`

```console
$ docker pull rethinkdb@sha256:f8814f4c012d9d3a64917cfdf649082852b1b05c49e651816a95c820c8cccd87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5bfce95e5fcd102d3301a0e3b1215ea41b948af8fff10753645cae32280f3044
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47990270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e957f5cf787c84123b2b33884c47a654bcb47e408510261763f43ef660e359fa`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:02:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 00:02:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 00:02:42 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:42 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 00:02:42 GMT
WORKDIR /data
# Thu, 12 Oct 2023 00:02:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 00:02:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3551f800fad0638fc92a6f5ef549613f1af07a0b944701476e29ccca0f6e1b`  
		Last Modified: Thu, 12 Oct 2023 00:02:56 GMT  
		Size: 6.3 MB (6331657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100bd3e3ecc342ed557ccbee8a0e093abacb5c0a17576aae93e2a88e47b68e03`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc67b92892290badfcfb51c38e3d52c817c823303bfa7c7e3dd28b8c457f753`  
		Last Modified: Thu, 12 Oct 2023 00:02:57 GMT  
		Size: 10.2 MB (10237936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99434c85cae415c01529e16d8296717499c8f642666970c860b4b9eb2c1cb9f4`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:3c0d354b06596850b3e649e76c143f9ef446e32e74e3ec8c4e1493db450b444b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45963331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45cef3ea38d82e1e8c329b04a79be65fb600af8bbeec3f0b3b0360f5f79c1a8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 11:55:16 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 11:55:18 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 20 Sep 2023 11:55:18 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 20 Sep 2023 11:55:22 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 11:55:22 GMT
VOLUME [/data]
# Wed, 20 Sep 2023 11:55:23 GMT
WORKDIR /data
# Wed, 20 Sep 2023 11:55:23 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 20 Sep 2023 11:55:23 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5778124bd581bd3873eb256ad673f582e8a92cc98314aa8637c701563c44aeb`  
		Last Modified: Wed, 20 Sep 2023 11:55:35 GMT  
		Size: 6.3 MB (6309724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a250dc6db71c0b2ff54f41a8947847840b7812db186713587a1cb1ad0914f59c`  
		Last Modified: Wed, 20 Sep 2023 11:55:34 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba55e90ddc0889cd7b15887445d45e01f413a447fa70752978fff882395933d`  
		Last Modified: Wed, 20 Sep 2023 11:55:40 GMT  
		Size: 9.6 MB (9587923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a7f8194d26b892763f4f886d194af681ae2e8c460abfa3001165727d634ad8`  
		Last Modified: Wed, 20 Sep 2023 11:55:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:b34358fbe9b8a0418977d30a4003c29e916e7df2b0930f89970fb0f25aa559a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45434194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f69055732c174b03f9bef05cd88c19adc4a68385db32bc1fc1e2ac541a32d7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 20 Sep 2023 02:54:54 GMT
ADD file:02a97e0d5f41f84ac0284849646284fa41b5e324d24f4d95bb1e2419899da811 in / 
# Wed, 20 Sep 2023 02:54:57 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 10:21:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 10:21:56 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 20 Sep 2023 10:21:56 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 20 Sep 2023 10:22:02 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 10:22:02 GMT
VOLUME [/data]
# Wed, 20 Sep 2023 10:22:02 GMT
WORKDIR /data
# Wed, 20 Sep 2023 10:22:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 20 Sep 2023 10:22:03 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:d2d51167e651784cce0bd658d0c2caa328adef8ccf264d8c09860a95bc2a2fc6`  
		Last Modified: Wed, 20 Sep 2023 03:00:22 GMT  
		Size: 29.7 MB (29653129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dea8e75d506a88101e35a004433cbbb4e0d816df67980894c1dee3b99163866`  
		Last Modified: Wed, 20 Sep 2023 10:22:19 GMT  
		Size: 6.2 MB (6205677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45ad7c29baadc14fbba254ba452aa26197aa54931d84a5106b2153cf5718bf6`  
		Last Modified: Wed, 20 Sep 2023 10:22:18 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf466c4d897f20b1e3f2dc68b7dd690a2db55c106023ae3799dab9a5745e2823`  
		Last Modified: Wed, 20 Sep 2023 10:22:19 GMT  
		Size: 9.6 MB (9572572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8866d2ff420286e20a0a3c316cdd2890071c9a1d078ab5c54150b58545cd03`  
		Last Modified: Wed, 20 Sep 2023 10:22:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
