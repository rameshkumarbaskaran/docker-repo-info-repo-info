## `clojure:temurin-8-boot-bookworm`

```console
$ docker pull clojure@sha256:de0fb69a58b6c979287b9dd8889d06fbfc06a24d6e535f139878b7a3df6be719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a0f6039608b1c9b4e3d08c96e526affacd180da2f4d0707be1f83b537df02c31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217520415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43b74a8ce35a4df9b6ba75da7ead9d3ae7c18a0395484dbae4d0d2862da8c7c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:27:34 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:27:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:27:35 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 01:27:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:27:35 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:27:42 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 01:27:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:27:43 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 01:28:02 GMT
RUN boot
# Fri, 13 Oct 2023 01:28:03 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de82c0f73ff6fa256f1fe1c33f18ffe9340b6034d90e0f84a2b65951b4e4920`  
		Last Modified: Fri, 13 Oct 2023 01:44:19 GMT  
		Size: 103.6 MB (103585016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cfe8bbe335f97ac48bc84243878698148cdcf9949bd96448c4419f1f10112b`  
		Last Modified: Fri, 13 Oct 2023 01:44:11 GMT  
		Size: 5.5 MB (5532646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cf27298774369433ce3292aa39b32b63143a4cf16ba104d40d02207c14ce6e`  
		Last Modified: Fri, 13 Oct 2023 01:44:14 GMT  
		Size: 58.8 MB (58820529 bytes)  
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
