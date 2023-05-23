## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:6d48c7fbff2c42fc4e8b06191523333d9893a01d6b1596bf107a725edf8fcf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4930abcf825b976783b24ec7e97222e213bfe930d1cc2ff7bcc6501fad895548
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170873579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e49dee77920a041afce8ae3b8f0fe49cde8971998a62b1693572e86f8f4106`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 23 May 2023 01:20:00 GMT
ADD file:150a6453ab2258061c1a1549ab119df752bdc2c2c84028fa0e83a0663cd8cedf in / 
# Tue, 23 May 2023 01:20:01 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:04:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 08:04:28 GMT
COPY dir:715eb4123a1bd94a1f232c902a6f3cdcc4011195a3e566c0f0ddc35dd1e83095 in /opt/java/openjdk 
# Tue, 23 May 2023 08:04:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:04:28 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 23 May 2023 08:04:28 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 23 May 2023 08:04:28 GMT
WORKDIR /tmp
# Tue, 23 May 2023 08:04:34 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 23 May 2023 08:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 23 May 2023 08:04:34 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 23 May 2023 08:05:00 GMT
RUN boot
# Tue, 23 May 2023 08:05:01 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bd73737482dd5575526c7207872963479808d979ab2741c321706b8553918474`  
		Last Modified: Tue, 23 May 2023 01:23:46 GMT  
		Size: 55.0 MB (55049027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565fb2e9c108d83ca7e7f2f21b31b868f54c4efeb86ac7d81e6201230801ffc3`  
		Last Modified: Tue, 23 May 2023 08:15:08 GMT  
		Size: 54.6 MB (54642112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3211f71e6b3b705ceb75a89d643b7db5259fc34008ad93be4e68316b4fd5dfb`  
		Last Modified: Tue, 23 May 2023 08:15:03 GMT  
		Size: 2.4 MB (2361847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22d415ad0bf4236f18126a24343222a27a8cb0d8d4f2a20db9ca4a4e8d4ab87`  
		Last Modified: Tue, 23 May 2023 08:15:05 GMT  
		Size: 58.8 MB (58820593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ae03b53cf9eb41a6e1bcf9f661a8cb642ca625f52ddd0c803a9090c8cb34dc72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168607130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9474315b574e4667b3cccbe6a88fcb7355a7c2d5b6ad231e2d9f427829c2b7`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 23 May 2023 00:43:08 GMT
ADD file:a823391455122220a061ff349b66ee33413e968447ec5ba4bd544d9182fa2fbe in / 
# Tue, 23 May 2023 00:43:08 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:24:11 GMT
COPY dir:f6bbe63c81e220d954915791686219263d8c45918fd81b238f7c9f6b21f076f8 in /opt/java/openjdk 
# Tue, 23 May 2023 01:24:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 01:24:12 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 23 May 2023 01:24:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 23 May 2023 01:24:12 GMT
WORKDIR /tmp
# Tue, 23 May 2023 01:24:17 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 23 May 2023 01:24:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 23 May 2023 01:24:18 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 23 May 2023 01:24:50 GMT
RUN boot
# Tue, 23 May 2023 01:24:51 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:b04fae59f135dd79280e4a6da39408e04c6d703c617cbcb1c524dfe6f2962fe5`  
		Last Modified: Tue, 23 May 2023 00:45:45 GMT  
		Size: 53.7 MB (53692612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec933d3080ef0a9a725f147ed686986ad36ef60808bf5f0ed2091007522988c`  
		Last Modified: Tue, 23 May 2023 01:34:03 GMT  
		Size: 53.7 MB (53742673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3070959a9f233868fc78ef05bae1acb49aba6d3df875b0f4e7cf339f7e6715fd`  
		Last Modified: Tue, 23 May 2023 01:33:59 GMT  
		Size: 2.4 MB (2351112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529d8976c41b9274b951b8bcfeee0fd4e000a4228ff878962f98c816f7ec201`  
		Last Modified: Tue, 23 May 2023 01:34:01 GMT  
		Size: 58.8 MB (58820733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
