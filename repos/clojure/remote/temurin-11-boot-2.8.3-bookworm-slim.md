## `clojure:temurin-11-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:eed0d58d5c68f850d4e098baf7d8e632dd46f95ed908912abf6b5549bd9cf7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b6c524aa4cd6dbaecb57a27df81831b9192ec72cf22506714297d8bb5bbd8a88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236738478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb96cda05d5feabd9f66098590d1e9d118b1eddda2f66d4a70ace8936288490`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:12:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:17:46 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:17:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:17:47 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:17:48 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:17:48 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:17:53 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:17:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:17:53 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:18:11 GMT
RUN boot
# Wed, 01 Nov 2023 01:18:11 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d63825152d5cbdd4aca989095ba3c4b2885c009fca2083969b63ead3b1ec3ae`  
		Last Modified: Wed, 01 Nov 2023 01:36:36 GMT  
		Size: 145.3 MB (145266659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a3b1b689ca11106462d75934f6959996cd5821172560f4acd45900e4457239`  
		Last Modified: Wed, 01 Nov 2023 01:36:25 GMT  
		Size: 3.5 MB (3501673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45acfbe193bdb64b92358ed9abb1e74d89fb1e0c7bdaa37138015721a1c335be`  
		Last Modified: Wed, 01 Nov 2023 01:36:28 GMT  
		Size: 58.8 MB (58820310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6fe28bfd7a1fbc880f4894a8c36229d40627431a80c77e4fce2f38ec1e6f4da3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233326531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b8d22d7775e3458227edc0866b5fbe98d860b7dc516ab403e3dd3d420a14c0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:57:22 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:57:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 00:57:26 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 00:57:26 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 00:57:26 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 00:57:31 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 00:57:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 00:57:31 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 00:57:48 GMT
RUN boot
# Tue, 31 Oct 2023 00:57:48 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eb29d768a9f4bddddbb15bd2381be6f475f0d817d5b776808080bd9b3d984e`  
		Last Modified: Tue, 31 Oct 2023 01:17:39 GMT  
		Size: 142.0 MB (142001972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca92f8e96d06f9ecb11e17d3c16e4936e07786b6a5964f90dabb81da6b2a399`  
		Last Modified: Tue, 31 Oct 2023 01:17:30 GMT  
		Size: 3.3 MB (3324901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f75a7842e1d793e6ba3dacac901df17a6f414a675f0a102c94f2b52b549137`  
		Last Modified: Tue, 31 Oct 2023 01:17:33 GMT  
		Size: 58.8 MB (58820374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
