## `clojure:temurin-8-boot-bookworm`

```console
$ docker pull clojure@sha256:75e8bd1b0694d4b078576c076e91d586207c45e22e7d3eb6006bcd842ab46517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2e71ae371def284ded8b756ee5734ebc47f22639400e28cf1cdbb767801404ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217518499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f015386276cefca320ec6c94dad5cf8c9e1ad84faf1d5d6ed751496afca3ff19`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:10:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:11:36 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:11:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:11:37 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:11:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:11:37 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:11:43 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:11:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:11:43 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:12:29 GMT
RUN boot
# Wed, 01 Nov 2023 01:12:30 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e319efa3c1ccba3860787f9c73906b26268d4cfba0f893ba6660f2ff59cdf0`  
		Last Modified: Wed, 01 Nov 2023 01:32:58 GMT  
		Size: 103.6 MB (103585059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794fd1cf14ddbb724ddf76b0f65dc0023bbb40c6122749bc60eaf29a2eb400d7`  
		Last Modified: Wed, 01 Nov 2023 01:32:51 GMT  
		Size: 5.5 MB (5530340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3475fe277c96e19a4c639a8a998e877ab05f8d8838a88e6fe7a715208b49f`  
		Last Modified: Wed, 01 Nov 2023 01:32:53 GMT  
		Size: 58.8 MB (58821076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6910286fa718fc202767da460adb5fe0fc8e68b359376cf9a72dbc3e03df28b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216479403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36076fd13b0d64091bb9a8aebcd19f8cc911fcf4401bf02b6c71dede9ea5889`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 00:58:44 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Fri, 13 Oct 2023 00:58:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 00:58:46 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 00:58:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 00:58:46 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 00:58:51 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 00:58:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 00:58:52 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 00:59:38 GMT
RUN boot
# Fri, 13 Oct 2023 00:59:39 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f775b99f3d26acccb021520058d84b450dc9bf368a53027ca58bcdb52b2eabe4`  
		Last Modified: Fri, 13 Oct 2023 01:13:16 GMT  
		Size: 102.7 MB (102690442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5c250744ae8d1306310c577db3dc66472a3ba4dd7d88b8d7e7c45f241a9433`  
		Last Modified: Fri, 13 Oct 2023 01:13:07 GMT  
		Size: 5.4 MB (5355481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5046c95d112d52c161d042baa064ecf7d9a172d124ab0ea3913051f5fc02caf3`  
		Last Modified: Fri, 13 Oct 2023 01:13:10 GMT  
		Size: 58.8 MB (58820902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
