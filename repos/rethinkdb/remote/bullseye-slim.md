## `rethinkdb:bullseye-slim`

```console
$ docker pull rethinkdb@sha256:89132d1340156cb4b9e4c2096a1b423f042fcd9180080127764ee8f9afe8d393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:b8c19ea4309426eb1629943621a50efb1bdc3bb7b5e10b6399f6f636d183a5d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47985048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4648138bfac8c18b1dfa5d490aa160ea669e6e246d605a991421ba8a0409051d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 09:13:25 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 09:13:27 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 04 Jul 2023 09:13:27 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 04 Jul 2023 09:13:33 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 09:13:33 GMT
VOLUME [/data]
# Tue, 04 Jul 2023 09:13:33 GMT
WORKDIR /data
# Tue, 04 Jul 2023 09:13:33 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 04 Jul 2023 09:13:33 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e81c4c52617b4910562167cd581451fa461f4a88bd721bef70f030d975e0b9`  
		Last Modified: Tue, 04 Jul 2023 09:13:47 GMT  
		Size: 6.3 MB (6328909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f27f163c2bde95a9c58843397ef3dd3d785c6322e4037ce13f5e67511dd2f5`  
		Last Modified: Tue, 04 Jul 2023 09:13:46 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685dcea274ee1816531b94cdba32445dfacdcad3f86c3e8b764efa05b62c888a`  
		Last Modified: Tue, 04 Jul 2023 09:13:47 GMT  
		Size: 10.2 MB (10235935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b78885a9ad557e720ec734b063c09324858951b01539714269005fa6201db5`  
		Last Modified: Tue, 04 Jul 2023 09:13:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:aceb40bb510fd238bc6c5a9c0dbfe4d86aac268741e8cef549eb123bc13575fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45963377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0962ca6a684fa21d2cbd5925090e3afd5c4b214f55a28671b8c24781bba75573`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:38:08 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:38:10 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 04 Jul 2023 06:38:10 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 04 Jul 2023 06:38:14 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:38:14 GMT
VOLUME [/data]
# Tue, 04 Jul 2023 06:38:14 GMT
WORKDIR /data
# Tue, 04 Jul 2023 06:38:15 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 04 Jul 2023 06:38:15 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e23d391375b2f2b14942a46fd484ecf6543bb68405e4fbf9a8499e689abe5fc`  
		Last Modified: Tue, 04 Jul 2023 06:38:28 GMT  
		Size: 6.3 MB (6309714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b271afd54c038a35d96fce1f200233e954e04702694766c7299254f1e4fb983`  
		Last Modified: Tue, 04 Jul 2023 06:38:27 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91551190fe418844731b03e86e87fc9ea75b9d66c2293713b0d84850e34b8a0f`  
		Last Modified: Tue, 04 Jul 2023 06:38:28 GMT  
		Size: 9.6 MB (9587892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9776923d73ebb8a8170bef7cdbecd107149465a5761b5df72dec059f42d4d342`  
		Last Modified: Tue, 04 Jul 2023 06:38:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:c3dc2d7121f6835e0c4b4c123e5c2591a263d3fab36effd40b9a8261496791c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45433643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7144da494e14b2b3a3fec43369c6f4184c112282024ef6cefcb06e62014caf2`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Jul 2023 01:32:44 GMT
ADD file:799c0afa70fa3bf4bb7804964481cba79e80aa3fad5c7a25beadde206ed6a8ff in / 
# Tue, 04 Jul 2023 01:32:46 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 15:29:15 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:29:18 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 04 Jul 2023 15:29:18 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 04 Jul 2023 15:29:23 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:29:24 GMT
VOLUME [/data]
# Tue, 04 Jul 2023 15:29:24 GMT
WORKDIR /data
# Tue, 04 Jul 2023 15:29:24 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 04 Jul 2023 15:29:24 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bbee891481f2623da9c7d37a49947926519c858c2b06773370a6189440d4b4de`  
		Last Modified: Tue, 04 Jul 2023 01:37:37 GMT  
		Size: 29.7 MB (29652540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d68900db98922447645c2cc554583c01a3e2a694c509242a91825dbc3829b23`  
		Last Modified: Tue, 04 Jul 2023 15:29:41 GMT  
		Size: 6.2 MB (6205715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b32ce839ea647eb94c2de63c246ff170767a6a3b46faf90655e9acb2c343326`  
		Last Modified: Tue, 04 Jul 2023 15:29:40 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c496f2632917e986f8daebbab33d2d6d13bf16457c1cecb6aa3a5493afa07332`  
		Last Modified: Tue, 04 Jul 2023 15:29:42 GMT  
		Size: 9.6 MB (9572574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e4129f50d6675ba63ab59750d612ba83b0a0d8277002e2cffcf3910ea9b142`  
		Last Modified: Tue, 04 Jul 2023 15:29:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
