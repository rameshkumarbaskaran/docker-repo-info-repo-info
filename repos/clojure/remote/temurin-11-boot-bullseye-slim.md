## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:a170fab9f781b714400055c623ca74c68dbf4bf023fc20193f4a0d4ca2b2c0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ece7f7c4f6cd0e106b154d4eb761c2c21293916a7d460f9f909348834b697b3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236141709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f18b8d04cf004f7087654c6a778603b590c7bd0aac9ef224c238ee19511194`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:37:40 GMT
COPY dir:ac445271830068829c3bd23eb1c86ee02cd9bb1649e3c49d8839a5a364b933c2 in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:37:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:37:41 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 03 Oct 2023 08:37:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 03 Oct 2023 08:37:41 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:37:47 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 03 Oct 2023 08:37:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Oct 2023 08:37:47 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 03 Oct 2023 08:38:06 GMT
RUN boot
# Tue, 03 Oct 2023 08:38:07 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9489ff926f0d6a8ba20abc78a9461fc70a87d4c0a043fb72a95b43934f07a8ac`  
		Last Modified: Tue, 03 Oct 2023 08:54:16 GMT  
		Size: 144.8 MB (144825998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798cc01a1acf123e38515227380ee8be3c08dfcb26deffe287ca595eb9d18c9a`  
		Last Modified: Tue, 03 Oct 2023 08:54:05 GMT  
		Size: 1.1 MB (1077538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8057fbeef2efc2e6f8a8c21a3f7a846f2038fd514c572fb3d65caace0d834d2f`  
		Last Modified: Tue, 03 Oct 2023 08:54:08 GMT  
		Size: 58.8 MB (58820462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1822a4ed796068eab0a9833d4bb07c7a977417abce3e88e4a526c576275aabd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231518908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7eda7c79038a9b8bd116774c0f9fc71e74ffdccaea50a2adceaf5f7f225a0b0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:48:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:29:03 GMT
COPY dir:17ac9e9d4b4d03adb229076835643ca11e6db9d9c122779536bfc61364556722 in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:29:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:29:06 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 03 Oct 2023 08:29:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 03 Oct 2023 08:29:06 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:29:11 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 03 Oct 2023 08:29:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Oct 2023 08:29:12 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 03 Oct 2023 08:29:29 GMT
RUN boot
# Tue, 03 Oct 2023 08:29:30 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1c21e56e06bf88aefd6edb1d9b40ca84fb99f8862f7f24beff9111809ec55d`  
		Last Modified: Tue, 03 Oct 2023 08:38:43 GMT  
		Size: 141.6 MB (141570687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5c225d05aae05301d90edd336d2f66dfc39e4920c97c0265fa34f10d87fbce`  
		Last Modified: Tue, 03 Oct 2023 08:38:34 GMT  
		Size: 1.1 MB (1064823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d1c4f5d96f45a904b5a91683b7a1f315419616e59b4f16010e05bc84be8b61`  
		Last Modified: Tue, 03 Oct 2023 08:38:38 GMT  
		Size: 58.8 MB (58820529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
