## `rethinkdb:2-buster-slim`

```console
$ docker pull rethinkdb@sha256:376a2383692ee7db54c6ff1690d0d2d52f995109a73a8a134811ff0ad541c80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7ffd078834e34d6d4aa8b48f880811a51a20b8b636265849029b601cb3bda718
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51839081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e00a7389678a26cf14cfc230095b079af1ec29b46526b1bb786b96491e1548d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:54:39 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:55:15 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 18 Mar 2022 08:55:15 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 18 Mar 2022 08:55:22 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:55:22 GMT
VOLUME [/data]
# Fri, 18 Mar 2022 08:55:22 GMT
WORKDIR /data
# Fri, 18 Mar 2022 08:55:22 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 18 Mar 2022 08:55:22 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd54f0ce44bc048a1f433fd61cd99c6e05b0b10f5b4596849de295998ed35ab`  
		Last Modified: Fri, 18 Mar 2022 08:55:48 GMT  
		Size: 6.7 MB (6690982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f50c2ea33e8fa34623bc0263bd0750ae0604986bdb218cdc761886e5dad3a9a`  
		Last Modified: Fri, 18 Mar 2022 08:55:46 GMT  
		Size: 2.6 KB (2611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d6b9a6af9b624d92a88920cddd12435937cb3ae7874867f401d7d89616455c`  
		Last Modified: Fri, 18 Mar 2022 08:55:49 GMT  
		Size: 18.0 MB (17991533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad606b4b832532a742ff85a859be920195ba59abd4e1e48dd51db290c906db59`  
		Last Modified: Fri, 18 Mar 2022 08:55:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
