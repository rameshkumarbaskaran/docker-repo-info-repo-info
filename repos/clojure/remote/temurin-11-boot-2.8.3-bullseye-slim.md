## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:7412624c829d07f971fa29ba97d4742557ea7ce61b1076e36ae29041c749fff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b81080409191674c653f1b451f3160b737239ba1cf7cea2b5e039e46779e3197
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289749328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c3b8dc2059f192a4601a0b03409b3282d28a9fc01dc60b4471aa63fc5371ef`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:54:03 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 01:54:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 01:54:05 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 21 Dec 2022 01:54:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 21 Dec 2022 01:54:05 GMT
WORKDIR /tmp
# Wed, 21 Dec 2022 01:54:11 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 21 Dec 2022 01:54:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 21 Dec 2022 01:54:11 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 21 Dec 2022 01:54:30 GMT
RUN boot
# Wed, 21 Dec 2022 01:54:30 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6db9c94a4957a1754107e38ff03b70c980e609a9f349a218009678a8917b1b7`  
		Last Modified: Wed, 21 Dec 2022 02:07:20 GMT  
		Size: 198.5 MB (198454552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5283604d8de6a9106851812fd34d45e511819ba968a783e1e5f50788c461ee67`  
		Last Modified: Wed, 21 Dec 2022 02:07:05 GMT  
		Size: 1.1 MB (1077338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98874b25a34a3aea6622817e5da7b1810c464f2fa525fb48400fd1d89ab9942d`  
		Last Modified: Wed, 21 Dec 2022 02:07:08 GMT  
		Size: 58.8 MB (58820495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cfb4f3f115af53637430e180ab49c65967c2991d40265da43141db66414c1923
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285150545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b64843c9a04faaa709cfc4d2444db7238946275436ffa59bdff1061a9d4cd4`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 05:04:05 GMT
COPY dir:e387a3b68139ff88bdac27d5ce097fc680f3cae9fdd88c28cdd91a06f9205180 in /opt/java/openjdk 
# Fri, 09 Dec 2022 05:04:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 05:04:09 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 09 Dec 2022 05:04:09 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 09 Dec 2022 05:04:09 GMT
WORKDIR /tmp
# Fri, 09 Dec 2022 05:04:14 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 09 Dec 2022 05:04:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 09 Dec 2022 05:04:14 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 09 Dec 2022 05:04:30 GMT
RUN boot
# Fri, 09 Dec 2022 05:04:30 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44bbb0380eb6b5cd1051003f5ce31baf496a9113c5e9927f76bcf714c433145`  
		Last Modified: Fri, 09 Dec 2022 05:18:38 GMT  
		Size: 195.2 MB (195203372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586a33c617d9a859a261455aac0fe9c9c611b0792c02b625cd8bffb638c7350e`  
		Last Modified: Fri, 09 Dec 2022 05:18:27 GMT  
		Size: 1.1 MB (1066319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c612765bf6d3af90e14436ba66ce0db6e66dcf38514c0a885037440b699c7b8d`  
		Last Modified: Fri, 09 Dec 2022 05:18:30 GMT  
		Size: 58.8 MB (58820534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
