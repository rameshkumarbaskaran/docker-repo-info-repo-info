## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:07d7f0298cb35c7f48125a1e7eddcef8e8981cbc55c40050058f9da08e7d493c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2c4a0772ccc5e65155f1cd07a366b9bdc717f7b297fc03faf166373f08b7dd24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170880770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422e8e19e8b745e18a9a9516456cd364d692d310ed2cbbec2b4abfea4c0e56fe`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:55 GMT
ADD file:b493776b6d91132ce50735e2d82076620774a1e0a690cf96777ddd6b85f513ef in / 
# Thu, 27 Jul 2023 23:24:55 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:13:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 03:13:49 GMT
COPY dir:715eb4123a1bd94a1f232c902a6f3cdcc4011195a3e566c0f0ddc35dd1e83095 in /opt/java/openjdk 
# Fri, 28 Jul 2023 03:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 03:13:50 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 28 Jul 2023 03:13:50 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 28 Jul 2023 03:13:50 GMT
WORKDIR /tmp
# Fri, 28 Jul 2023 03:13:55 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 28 Jul 2023 03:13:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 28 Jul 2023 03:13:55 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 28 Jul 2023 03:14:35 GMT
RUN boot
# Fri, 28 Jul 2023 03:14:35 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:9a9e034800a1747ea288f38f6087c036acac99dd3ec5255bf7798abd8c23a304`  
		Last Modified: Thu, 27 Jul 2023 23:29:45 GMT  
		Size: 55.1 MB (55055571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f2467027ab6a97b20105e61541ccde22023beb67dd246cdb940a2f15187d3c`  
		Last Modified: Fri, 28 Jul 2023 03:27:57 GMT  
		Size: 54.6 MB (54642111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f10820eb5b432c11ace8794aa4e3cf37e4618046c51600ed5e9634c752e0c0`  
		Last Modified: Fri, 28 Jul 2023 03:27:52 GMT  
		Size: 2.4 MB (2362133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca31f68a562aec5285fe072cfed1f94e6ca95c14cbaca698bda4f22901df7a2`  
		Last Modified: Fri, 28 Jul 2023 03:27:55 GMT  
		Size: 58.8 MB (58820955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:781e4a3ededd0e707e1c959334e10be77d951e8f019d8d4b6aac6dafedef11e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168618676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d83d0f8418fe8f9f63e036a4f9060b33070e0c3a780b75af2ec2454392c5fa3`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:43:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:43:39 GMT
COPY dir:f6bbe63c81e220d954915791686219263d8c45918fd81b238f7c9f6b21f076f8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:43:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:43:41 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 04 Jul 2023 06:43:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 04 Jul 2023 06:43:41 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 06:43:46 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 04 Jul 2023 06:43:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Jul 2023 06:43:47 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 04 Jul 2023 06:44:08 GMT
RUN boot
# Tue, 04 Jul 2023 06:44:08 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a952e7f7b69157dc62e9b0f020a4c17e46f7508fa5415a079eef7242d1af239c`  
		Last Modified: Tue, 04 Jul 2023 06:53:36 GMT  
		Size: 53.7 MB (53742700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e695322dfe4b16414bef56486531d3a286a348b604124654772e060291ffe8d3`  
		Last Modified: Tue, 04 Jul 2023 06:53:30 GMT  
		Size: 2.4 MB (2351391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bc81802e4d363864efb3d454664b6a1b7ae857963a83a5bd4bdcb4b40d9120`  
		Last Modified: Tue, 04 Jul 2023 06:53:33 GMT  
		Size: 58.8 MB (58820606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
