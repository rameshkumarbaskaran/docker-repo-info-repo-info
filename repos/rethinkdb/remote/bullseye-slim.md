## `rethinkdb:bullseye-slim`

```console
$ docker pull rethinkdb@sha256:7f9252adfe6231b9084bf6037fab6eccadc57b14b27653409faabbf819a06d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:1ea42e3f508e86a131ec7203f3059d834cc0828c48a95c42f4abd3b47281d2bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47971099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325ac0d70d22701aa2f30d30c7168c8a954af973f728d1511c0afeae93efc425`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:23:47 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 21:23:48 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 03 May 2023 21:23:49 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 03 May 2023 21:23:53 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 21:23:53 GMT
VOLUME [/data]
# Wed, 03 May 2023 21:23:54 GMT
WORKDIR /data
# Wed, 03 May 2023 21:23:54 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 03 May 2023 21:23:54 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4558e1e47f37b39bc785180ffed170a5f4e9257184e961102601cf4450ae95c0`  
		Last Modified: Wed, 03 May 2023 21:24:05 GMT  
		Size: 6.3 MB (6328844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ca2683dfe91cd43811b9493ee7e24c315c1b45891a1de23a20519e9b3001fe`  
		Last Modified: Wed, 03 May 2023 21:24:04 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfbc64fa2c3b36f796920020eed300a1ca8f1beaa6bb5612bcf4c5ce480d83fa`  
		Last Modified: Wed, 03 May 2023 21:24:06 GMT  
		Size: 10.2 MB (10235923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a58925f330f368409b66bd574c6c0a6a71488b166206262b83a6c4c0c72c3c`  
		Last Modified: Wed, 03 May 2023 21:24:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:97c4230d08ac9fbc3c031f8c810bb828d5731b2a2de2a8ad346e9e93044803b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45953137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fac1ae9fdc6e9d61a8c6f66c9c10479dcd514ffb6d17a96e734035e025364e3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:30:26 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:30:28 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 03 May 2023 18:30:28 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 03 May 2023 18:30:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:30:32 GMT
VOLUME [/data]
# Wed, 03 May 2023 18:30:32 GMT
WORKDIR /data
# Wed, 03 May 2023 18:30:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 03 May 2023 18:30:32 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb078617881c650879ddd46eb3cdfa91e38c015026cd670783804933b9de21de`  
		Last Modified: Wed, 03 May 2023 18:30:43 GMT  
		Size: 6.3 MB (6309708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef258d4f30af2b602534072b604720e411c306912e753a8ae672346eb66ed12b`  
		Last Modified: Wed, 03 May 2023 18:30:42 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3b03236fb9f50e7e68164242219ba1a1859d2531433e1363b4e3f77dbabe64`  
		Last Modified: Wed, 03 May 2023 18:30:43 GMT  
		Size: 9.6 MB (9587881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb111c99c796eb1f6a4107e16365e95055bead8c42f47bb96b51aa69667ad068`  
		Last Modified: Wed, 03 May 2023 18:30:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:c99b8dc78f9e43b6615f724fccbf1fb57baf6145430ec2e9952b429de6f2e8fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45423494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6a1f5d6eb5060651ef29b13503d1c4f5fce03cea6560feb81104679c43c446`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 03 May 2023 03:41:57 GMT
ADD file:7dcdb7d695d9510a1a7e1623776d63d56f7025bdd1702a13a3acd52af825b9c3 in / 
# Wed, 03 May 2023 03:41:59 GMT
CMD ["bash"]
# Wed, 03 May 2023 23:10:45 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:10:48 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 03 May 2023 23:10:48 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 03 May 2023 23:10:54 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:10:55 GMT
VOLUME [/data]
# Wed, 03 May 2023 23:10:55 GMT
WORKDIR /data
# Wed, 03 May 2023 23:10:56 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 03 May 2023 23:10:56 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:8e4cb8eb5d7a86a02dfc1d3645e982def0fc1c20e1fd14d9c6736177d3887dfa`  
		Last Modified: Wed, 03 May 2023 03:44:59 GMT  
		Size: 29.6 MB (29642157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a27710b78f8c26577da86a3dbd57bf670c8ccc148932cff1f8c36697ffc1c2`  
		Last Modified: Wed, 03 May 2023 23:11:11 GMT  
		Size: 6.2 MB (6205859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fdd88975b37d148e306c8018964eebf5e70abc207c98572ab496f3a992ee96`  
		Last Modified: Wed, 03 May 2023 23:11:10 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db55cdfe3cc9951a9aae6dd18b568eebb201b051d0c0ce7476b8edc6c58efa42`  
		Last Modified: Wed, 03 May 2023 23:11:12 GMT  
		Size: 9.6 MB (9572664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d4843e9b01e416e0127202305d52923b91213c0f6eb140dcf39736b5d3a23c`  
		Last Modified: Wed, 03 May 2023 23:11:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
