## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:60e737197143e02ca9bb367528d37d9eaeb328618c8a24e1eb1e86ec5829c153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:43bd6bc93f433de3d851cee3f78a5f7cd79b30ce745650117762786200750aed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236192099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043e35bc0220cf939677b0e09cff86bfec3e562e1e2aa8c7e319431ff00154ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:24:07 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:24:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:24:09 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:24:09 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:24:09 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:24:14 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:24:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:24:15 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:24:32 GMT
RUN boot
# Wed, 01 Nov 2023 01:24:32 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Nov 2023 01:24:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Nov 2023 01:24:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c20750b154d64794fedb0a429e74999708e8bd1d859c9bc36ca5afefa982a25`  
		Last Modified: Wed, 01 Nov 2023 01:40:50 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca171bb7e3ff6aa4915f43b447aa09dac67ee24a6968935535ff8b9e5f87c77`  
		Last Modified: Wed, 01 Nov 2023 01:40:39 GMT  
		Size: 1.1 MB (1079475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9944ef504e123b00e91c92a914fe738097ac291c8ebb1748aa7f7a875ddea52f`  
		Last Modified: Wed, 01 Nov 2023 01:40:43 GMT  
		Size: 58.8 MB (58820405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b44023328fcd85c7aec7380109043190dffea59745b185d4ebe7a503b33cb6`  
		Last Modified: Wed, 01 Nov 2023 01:40:39 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8aab8b5b2f83b06a8f48486cebd7ba3c1cc52f1faec1600f6a1aa467cd6f06d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233633154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc0a2955fc5144de091f0755dff90f4528c8c41f7dc41de8c5a650f9bdf220d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:23:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 02:33:06 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Wed, 01 Nov 2023 02:33:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:33:10 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 02:33:10 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 02:33:10 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 02:33:15 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 02:33:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 02:33:15 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 02:33:32 GMT
RUN boot
# Wed, 01 Nov 2023 02:33:32 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Nov 2023 02:33:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Nov 2023 02:33:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cca082400e47c6a11576684f6f97eebdf67ba34cbf7e1a6a23a5fdf35fbc01`  
		Last Modified: Wed, 01 Nov 2023 02:48:27 GMT  
		Size: 143.7 MB (143681748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40160b31142ac6e0d75a25743149aa8bbf96e5d86eb842fe6803ca5465a05d9`  
		Last Modified: Wed, 01 Nov 2023 02:48:18 GMT  
		Size: 1.1 MB (1066853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e09615c3deb418a32c858c588f3698b2bc60f559d9e55c742d2682567900f3`  
		Last Modified: Wed, 01 Nov 2023 02:48:21 GMT  
		Size: 58.8 MB (58820250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0390bead52366c0082e7ba5b1c0d37d1affc48c4c4e5836113c85bc951533eae`  
		Last Modified: Wed, 01 Nov 2023 02:48:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
