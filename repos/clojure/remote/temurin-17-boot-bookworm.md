## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:bddadb46791a75a435218685e25ad11f8e7f96e50049186b146d8054cecf02fb
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
$ docker pull clojure@sha256:795932e7371c59357eee1ca354bd6d3b5cd231838b90c2d2631a51b7a1f0dfbe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257468595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5191b5ec28ea91f05c6d37e75cea4d41365d9183d7b126620003102989328c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:30:54 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 07:30:58 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 07:30:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 07:30:58 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 07:31:03 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 07:31:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 07:31:03 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 07:31:20 GMT
RUN boot
# Tue, 21 Nov 2023 07:31:20 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 21 Nov 2023 07:31:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Nov 2023 07:31:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb7eea93e806cda12688c1cef1abab3769a83178187c1b5813f675ffa83e80f`  
		Last Modified: Tue, 21 Nov 2023 07:46:23 GMT  
		Size: 143.7 MB (143681765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b52823e9078733a1d076bdcd536e0130aae8752ae432c8fad250890e3a8be4`  
		Last Modified: Tue, 21 Nov 2023 07:46:15 GMT  
		Size: 5.4 MB (5353254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e07380d64e9ed9342c1a721b5a246a89ee35edd40b56a97f52a8331ef321af5`  
		Last Modified: Tue, 21 Nov 2023 07:46:17 GMT  
		Size: 58.8 MB (58820526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26df355d1454b14e819e1b929adb734630f8567d461cbebdb88b83f47a6a81e8`  
		Last Modified: Tue, 21 Nov 2023 07:46:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
