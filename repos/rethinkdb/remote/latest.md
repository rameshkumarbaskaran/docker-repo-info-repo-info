## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:c928f928a042b71e28b25a495881261113fee9c1c7e3f532486ec4d61f8b1487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:cd671fce661da6226abe222eb3ec3214f5960dd4820ad0cca21f6fbbda08419c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47971210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f6e9a82d8274164b290e444fa59b57b6d16f8cb9d749555d0dbe1c4ff6a14c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 11:14:01 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 11:14:03 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 23 May 2023 11:14:03 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 23 May 2023 11:14:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 11:14:08 GMT
VOLUME [/data]
# Tue, 23 May 2023 11:14:08 GMT
WORKDIR /data
# Tue, 23 May 2023 11:14:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 23 May 2023 11:14:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d12610eded15f7001db65f4bed57a0d51651766f3539e5d23ff862f71f45fb`  
		Last Modified: Tue, 23 May 2023 11:14:20 GMT  
		Size: 6.3 MB (6328868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bac44350ea0f11b7463691bd61353c9939e91773e4d68113fdd21f66802afe7`  
		Last Modified: Tue, 23 May 2023 11:14:19 GMT  
		Size: 2.7 KB (2685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d188636bbe045a23e00f0c9a0eda422e9f95470e424fe3e5d205be6ed157bcd`  
		Last Modified: Tue, 23 May 2023 11:14:21 GMT  
		Size: 10.2 MB (10235948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa66d1fa04cb4c739a33947d67408317d404f8fdd15449f1c6c5d25329fda8a9`  
		Last Modified: Tue, 23 May 2023 11:14:19 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:142af303895c7d587b3777393e67a3af1cb1453cd20d5ee6f47198c534618aa2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45953178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b690dec9c7866b4baf0e42ddd7e810d13ab7f8144c4d7ede7ef19ec873183d9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 07:21:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:21:35 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 23 May 2023 07:21:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 23 May 2023 07:21:40 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:21:40 GMT
VOLUME [/data]
# Tue, 23 May 2023 07:21:40 GMT
WORKDIR /data
# Tue, 23 May 2023 07:21:40 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 23 May 2023 07:21:40 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8f3f3494686d186f7378275ce40dd8033f0b5cce03cd99cc2beb869ae008f3`  
		Last Modified: Tue, 23 May 2023 07:21:51 GMT  
		Size: 6.3 MB (6309707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318bdfc8c82fa4a91074b8966f9477c658310411d6edabe0fa0d345345c764c6`  
		Last Modified: Tue, 23 May 2023 07:21:50 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f356ec4314c8cc773fe6f1544a1463e0f01d8c10825251dd8624445e31d32df7`  
		Last Modified: Tue, 23 May 2023 07:21:52 GMT  
		Size: 9.6 MB (9587907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12847fc9b2124b07a874e41abe8eb64243f46430a2cd40f184c4d5b2b5f5796d`  
		Last Modified: Tue, 23 May 2023 07:21:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:22557d08fe58192b31fdfae921d7745d227da390602d8c8a54090eb68eece3ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45423288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9ae3528fe5586a2fe1c778a3ccadc3e71e9209601c9588d9cf3ad3397c428e`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 23 May 2023 00:42:52 GMT
ADD file:23b1e12559302529556a94a1d4098dbdb454e263265258b940c2b2d23a97c121 in / 
# Tue, 23 May 2023 00:42:54 GMT
CMD ["bash"]
# Tue, 23 May 2023 03:49:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 03:49:57 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 23 May 2023 03:49:57 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 23 May 2023 03:50:02 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 03:50:02 GMT
VOLUME [/data]
# Tue, 23 May 2023 03:50:03 GMT
WORKDIR /data
# Tue, 23 May 2023 03:50:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 23 May 2023 03:50:03 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:9c24ec455bdb6a9ad0d033c7cce8e71dd5bdbbe53a86d5feeb8d4cb7804fb8e5`  
		Last Modified: Tue, 23 May 2023 00:45:47 GMT  
		Size: 29.6 MB (29642170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a884639842a2930a09761e999c5c5fcfbddf6348457d33fcf34ddc41cfa660`  
		Last Modified: Tue, 23 May 2023 03:50:16 GMT  
		Size: 6.2 MB (6205713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfcc5c874f941e100525685c510a0bba1a423c0e48a7f7dbd9f7c4ae3341f7e`  
		Last Modified: Tue, 23 May 2023 03:50:15 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a850cb2528ec59d74422e7b64a0ff5d00aa468d67a59640ff92e66ebf6f9a3`  
		Last Modified: Tue, 23 May 2023 03:50:16 GMT  
		Size: 9.6 MB (9572589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f1d545bb005f5f1c95b13226121a0ad01f092db5fb9d3b19d434e86fc7d2b`  
		Last Modified: Tue, 23 May 2023 03:50:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
