## `clojure:temurin-17-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:cf5ef42449178937a2a4cf32ca61a7f8b86531e6c0eb15b13ad30e73605fa4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bookworm` - linux; amd64

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

### `clojure:temurin-17-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:08af62daf7df0c72552a7bc4e98779995e752b99320035ad87aa01a233ceeecc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257468296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bd9d5c640bff64913ae714c28eb6bd02812c65d89af984db61f8422f562769`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:04:55 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 01:04:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 01:04:58 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 01:04:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 01:04:59 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 01:05:04 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 01:05:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 01:05:04 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 01:05:22 GMT
RUN boot
# Tue, 31 Oct 2023 01:05:22 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 31 Oct 2023 01:05:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 31 Oct 2023 01:05:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8e5e52e2f4027035c0b4ddc5b921034970f50db7c28155054a83132fbde7fe`  
		Last Modified: Tue, 31 Oct 2023 01:22:19 GMT  
		Size: 143.7 MB (143681763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accadede649a38524344312734d2daaa67f32761fbbaa3be0cf71b6b15c4ab95`  
		Last Modified: Tue, 31 Oct 2023 01:22:10 GMT  
		Size: 5.4 MB (5353199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084eb06903470ea283650cc84f73e6b02a9d0b9dce0081006f88194e20a7018c`  
		Last Modified: Tue, 31 Oct 2023 01:22:12 GMT  
		Size: 58.8 MB (58820356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d195559c1a2c3d65a92cc251809bc781a9bf130dc7a7d6a24b47e75702529fc`  
		Last Modified: Tue, 31 Oct 2023 01:22:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
