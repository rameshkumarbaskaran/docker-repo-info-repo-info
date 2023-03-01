## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:de0efb0db81fc5c12d009b902ba112dcafd241b28df7c7563893cacb3ce29c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a345ab29166a5c5add76fb216111415ed86821186c177cf26bb6be45d2592a57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283748130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b66b0a921368732e0981678e1ea88430d91bf163e56bd35998a623051d26daf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:22:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Feb 2023 09:28:39 GMT
COPY dir:5cf52f938fe415b0022fbccb8cf978562c503c0b8313cc9dedf46c1c4edb35cf in /opt/java/openjdk 
# Thu, 09 Feb 2023 09:28:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 09:28:41 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 09 Feb 2023 09:28:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 09 Feb 2023 09:28:41 GMT
WORKDIR /tmp
# Thu, 09 Feb 2023 09:28:46 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 09 Feb 2023 09:28:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Feb 2023 09:28:46 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 09 Feb 2023 09:29:04 GMT
RUN boot
# Thu, 09 Feb 2023 09:29:04 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 09 Feb 2023 09:29:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Feb 2023 09:29:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c81d82cb4b2b71263b3117ae53e60d87a90991c692f5ff54bea94797fdf512`  
		Last Modified: Thu, 09 Feb 2023 09:40:40 GMT  
		Size: 192.4 MB (192438189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b05bab1b9ba30681ad47120bffd01bb1d2b56b4564173f929a1b09b1530f9b6`  
		Last Modified: Thu, 09 Feb 2023 09:40:26 GMT  
		Size: 1.1 MB (1077346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b743d0fa3de07875198f7a3a0b0e14403920c356a4971f83ff5c8271e504d1`  
		Last Modified: Thu, 09 Feb 2023 09:40:29 GMT  
		Size: 58.8 MB (58820384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832a62b8bad23e713d2a654a7ad60be209722563b8a0386cbfeb89a476d2127b`  
		Last Modified: Thu, 09 Feb 2023 09:40:26 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8f9b03acdaf4a303b8e69a27d14a6cee7164f48e45c1ba5fd3a40a0a0c7d8c73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281208889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547de7ad3548dce6431668f547d78690266c2c4b4658254610cb4c397f153feb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:07:09 GMT
COPY dir:a1bd99c3d82513db94430c73467e1e5c69ea4624d0489571d594afe503e15dc5 in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:07:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:07:13 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 03:07:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:07:14 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:07:18 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 03:07:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:07:18 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 03:07:36 GMT
RUN boot
# Wed, 01 Mar 2023 03:07:36 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 03:07:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 03:07:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fea299b8494f8b0756cbfb644eec65ca18c102ef09fafc09ea59e9d201162b5`  
		Last Modified: Wed, 01 Mar 2023 03:17:40 GMT  
		Size: 191.3 MB (191260427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f02eda8a922dd7120c09b57f9c839d9bca5c9ba62784009164ddae4e02e22d7`  
		Last Modified: Wed, 01 Mar 2023 03:17:28 GMT  
		Size: 1.1 MB (1064589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a42c2ee0d57f2d4b6cb4d63afa8abd094e3e6d466d36c655bcdf077ed77de3`  
		Last Modified: Wed, 01 Mar 2023 03:17:30 GMT  
		Size: 58.8 MB (58820661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4daadb5ee5298ac620c66d9ed8a6be116a8cf3ee371c410de0eae9f4e3ba8f`  
		Last Modified: Wed, 01 Mar 2023 03:17:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
