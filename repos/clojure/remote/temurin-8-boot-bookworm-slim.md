## `clojure:temurin-8-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:b761dad92917d7b0ad8dd61a372572ef364e632d0befe99b8ed2a8b318bbd81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:26cefed11947e3d16614034ea3d16fcb3a190720201cb642301af6e39dd1d330
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195070141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9250b007e321732f2cd4dc9860273da6a435f62955a595930921cf83c5969c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:12:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 01:50:31 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 02 Nov 2023 01:50:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 01:50:31 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 02 Nov 2023 01:50:31 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 01:50:32 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 01:50:37 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 02 Nov 2023 01:50:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 01:50:38 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 02 Nov 2023 01:50:56 GMT
RUN boot
# Thu, 02 Nov 2023 01:50:56 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a218e9c40dab330f555e00fbdf54bbc4a1c72977e72f15e20a344c6eb36f3`  
		Last Modified: Thu, 02 Nov 2023 02:02:58 GMT  
		Size: 103.6 MB (103598265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bb7e9ce92e0c6509ed2d59bea352401f52141c287b79c515d1f4aad6c14f15`  
		Last Modified: Thu, 02 Nov 2023 02:02:50 GMT  
		Size: 3.5 MB (3501673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfde9fe408c5b28240a9a20d466c8b1c112bba1a268b49ca0c7a3fb52bb3e79`  
		Last Modified: Thu, 02 Nov 2023 02:02:53 GMT  
		Size: 58.8 MB (58820367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad10c0f796ade404e9a872347d99a7b528979deb3d5ad9c37d3b072d31efb66d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194026231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280dec886d018afd5561e3cc7b54e0d41c03fd38ebab84f0d2d0876249f356ba`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:22:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 03:28:42 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Thu, 02 Nov 2023 03:28:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 03:28:44 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 02 Nov 2023 03:28:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 03:28:44 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 03:28:50 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 02 Nov 2023 03:28:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 03:28:50 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 02 Nov 2023 03:29:08 GMT
RUN boot
# Thu, 02 Nov 2023 03:29:08 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b95ba4f42cf700bc15c43f945df7888a3f1517eba974a7407a4876a247f3eb1`  
		Last Modified: Thu, 02 Nov 2023 03:38:23 GMT  
		Size: 102.7 MB (102701531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e1edb78a33e6347c52d1eb1db7e774b64424bd6c89ee3fd4587a76491328dc`  
		Last Modified: Thu, 02 Nov 2023 03:38:17 GMT  
		Size: 3.3 MB (3324921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7417e9865818842e42912037ea8db395759f893879217519d7b8d341c73da68d`  
		Last Modified: Thu, 02 Nov 2023 03:38:19 GMT  
		Size: 58.8 MB (58820660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
