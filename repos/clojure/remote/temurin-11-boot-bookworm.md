## `clojure:temurin-11-boot-bookworm`

```console
$ docker pull clojure@sha256:d08e65910785e693a383c2a1abd20762632afe4d546b4fe56f07285ffd6ff589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9c7624b5dfbc259c3df6fea2c7147ec4dd902b1201254274b3e67b3fb2d4a3d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259199441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2033d291fac96ad13021fe41401078974af436db7a703ee91ec8c169927331a6`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:10:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:17:13 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:17:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:17:14 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:17:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:17:14 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:17:20 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:17:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:17:20 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:17:38 GMT
RUN boot
# Wed, 01 Nov 2023 01:17:38 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52bf082e2f57af3aac777d96ce5e6d17154d3e9980eb8b5ffbaffaa59e38fbe`  
		Last Modified: Wed, 01 Nov 2023 01:36:16 GMT  
		Size: 145.3 MB (145266685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1a9d05a5fb80d9917a7e58b95bd82a7af477adb42577afd8dd702f26bd930a`  
		Last Modified: Wed, 01 Nov 2023 01:36:06 GMT  
		Size: 5.5 MB (5530422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243ffd243dc874d102b5ec78b7fbf5de2c93e6423913872a783c5743a2e0f615`  
		Last Modified: Wed, 01 Nov 2023 01:36:09 GMT  
		Size: 58.8 MB (58820310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1a1aaaabb87e407694f80f6d6d56b313227765eb5ba42b49ccb4c802882ce38f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255788322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d43b8044ce3d70b80c1b054ef14cee8983ac16acdd83d7c9c3c40bab05c3f9c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:21:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 02:26:32 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Wed, 01 Nov 2023 02:26:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:26:36 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 02:26:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 02:26:36 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 02:26:42 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 02:26:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 02:26:42 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 02:26:59 GMT
RUN boot
# Wed, 01 Nov 2023 02:26:59 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d79c35290d56eefd772281c4af56c3f36d944e9abd9cd9418a0a92e398e8d9`  
		Last Modified: Wed, 01 Nov 2023 02:44:16 GMT  
		Size: 142.0 MB (142001939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434b366628a36fd4adb349c0fe0b205eda218ed38174feb52f55c8ac2ef9d17`  
		Last Modified: Wed, 01 Nov 2023 02:44:08 GMT  
		Size: 5.4 MB (5353291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192d7dd5b29d6945d9a6e808757c75cc32112a31663b644141d8dc7ce6b6725d`  
		Last Modified: Wed, 01 Nov 2023 02:44:11 GMT  
		Size: 58.8 MB (58820439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
