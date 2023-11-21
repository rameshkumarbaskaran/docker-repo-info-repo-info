## `clojure:temurin-11-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:fdc2b9e0c39942627975d6e7dff7921b02b304b527c3dbdd65d52c614601f284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0053ef119e6d15a5ed344ffc1649f10dadad63145593ab3c2a8f10c4d4d9649c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236738772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ca282ee97e5be470bcaca653abcb08a179dac05f9b8770365977f3a2303791`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:08:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:14:14 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 21 Nov 2023 10:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 10:14:15 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 10:14:15 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 10:14:15 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 10:14:21 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 10:14:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 10:14:21 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 10:14:37 GMT
RUN boot
# Tue, 21 Nov 2023 10:14:38 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dc1244222edb818298f70a56cf7bed949c04ed09420e025c3cfb77a74e8d07`  
		Last Modified: Tue, 21 Nov 2023 10:32:14 GMT  
		Size: 145.3 MB (145266681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b84adfa88bf2187743d3dd2d294f5d6d72cd2df696e6a9661bd4bb96a6f8da`  
		Last Modified: Tue, 21 Nov 2023 10:32:04 GMT  
		Size: 3.5 MB (3501708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251664e094eaadb65cf2e57d494e2945a728dc872743eb38f3e77213c3b2dbc4`  
		Last Modified: Tue, 21 Nov 2023 10:32:07 GMT  
		Size: 58.8 MB (58820475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:47850e4ba2b580eee75dbbb600c5543e418c232bf795d13c7824a6073de02342
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233326583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38367c4bd711718b4288005e36bc5e8bb01336959c86f42f7e7d8878c9ebe9e3`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:26:48 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:26:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 07:26:51 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 07:26:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 07:26:51 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 07:26:56 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 07:26:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 07:26:56 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 07:27:12 GMT
RUN boot
# Tue, 21 Nov 2023 07:27:13 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7380b182fb0ab44680e2ae8a99d8a7c4ea84bd6ac7e36e717f150191d6d29339`  
		Last Modified: Tue, 21 Nov 2023 07:43:19 GMT  
		Size: 142.0 MB (142001953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e295624045a2964b5e58518a1f1fbc0f1c2c5f05c87cdb24f1636d3baa9750`  
		Last Modified: Tue, 21 Nov 2023 07:43:11 GMT  
		Size: 3.3 MB (3324896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556617924c1477410f11a3d22bc11d77ed3745aaef5830646d39e60c3d5ea177`  
		Last Modified: Tue, 21 Nov 2023 07:43:13 GMT  
		Size: 58.8 MB (58820457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
