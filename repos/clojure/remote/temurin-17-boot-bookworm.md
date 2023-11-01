## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:79c645460fe5e323f59ced6e66f60cf6804468819342f45e1f55cb9e2fddedb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:15b28108fc7553df05034db089864684e98c09a0ac0558f67825bcde2d7110ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258807003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d010c7003c98f43f4fcefb4279b7ee759aafc70451c133e847f05612ff71446`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:10:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:22:31 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:22:32 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:22:32 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:22:32 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:22:38 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:22:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:22:38 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:22:56 GMT
RUN boot
# Wed, 01 Nov 2023 01:22:56 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Nov 2023 01:22:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Nov 2023 01:22:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a05faf0cd98c5e3023b81d5851ba37c4093d2fdd6da9fc527471ac1aa01955`  
		Last Modified: Wed, 01 Nov 2023 01:39:48 GMT  
		Size: 144.9 MB (144873950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c53db9e21b13e68dec22cee208e27378484ff831cbdc595c91e8e0cfc22d25`  
		Last Modified: Wed, 01 Nov 2023 01:39:37 GMT  
		Size: 5.5 MB (5530281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5dac4f107905750230ea0edec1209031fa3b39994743b66f6ef1c0dce16bbe5`  
		Last Modified: Wed, 01 Nov 2023 01:39:41 GMT  
		Size: 58.8 MB (58820349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e572b390f11a09a4eec9fc7142af3caafc491f78faa0cc4a39e8912a0ebbc7ee`  
		Last Modified: Wed, 01 Nov 2023 01:39:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e896939efd180653234ff0f7d74da0cefa5911d7b550d6f4fa349d17040c2145
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257468495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669c6ffa652826fea5e4d1fe870fe8744fcd8152b4175aacfc8d6dc22c7a6c04`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:21:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 02:31:27 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Wed, 01 Nov 2023 02:31:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:31:31 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 02:31:31 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 02:31:31 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 02:31:37 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 02:31:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 02:31:37 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 02:31:54 GMT
RUN boot
# Wed, 01 Nov 2023 02:31:55 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Nov 2023 02:31:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Nov 2023 02:31:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95ffb8e5d195afda304b9f8d3154a67ff29e99daad616b25566a79f341bb6bd`  
		Last Modified: Wed, 01 Nov 2023 02:47:31 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621b1b2dd9bb7a0ba2ed9119c3d8e46aa64627f52ccc8fb369ff82543d6b08a5`  
		Last Modified: Wed, 01 Nov 2023 02:47:22 GMT  
		Size: 5.4 MB (5353218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d63d3573319f86a4bef66ad6eb6f9769325745f167001edec65dbe655dde5f`  
		Last Modified: Wed, 01 Nov 2023 02:47:25 GMT  
		Size: 58.8 MB (58820512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03288a9d42feb7132c996379d99379f628493bbb1324c07d1eee7588674b622`  
		Last Modified: Wed, 01 Nov 2023 02:47:21 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
