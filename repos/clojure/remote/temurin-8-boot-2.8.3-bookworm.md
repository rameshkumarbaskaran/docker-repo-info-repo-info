## `clojure:temurin-8-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:1c327a711f1ef80b80369d91471d5da1522b079fcb93aa26588d58c35f0e5465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9deb9083bc8e37c94dfffb01f78d83ee29660ed2b4f427e78ceadce576f372b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217531921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4656aa4102103fe37e146106ed5a4f80f1fd56cfe4aca50584f28b8a0c2d2ac1`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:10:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 01:49:21 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 02 Nov 2023 01:49:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 01:49:22 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 02 Nov 2023 01:49:22 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 01:49:22 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 01:49:30 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 02 Nov 2023 01:49:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 01:49:30 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 02 Nov 2023 01:50:22 GMT
RUN boot
# Thu, 02 Nov 2023 01:50:23 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb39566a75265042a4da46fe895a549775ce2e985de2d6c4feb658793a1d88e`  
		Last Modified: Thu, 02 Nov 2023 02:02:40 GMT  
		Size: 103.6 MB (103598249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c67f148d6c8cf8d8c90614328bd1a1e1fe644f38cdcfd81dea7210dedd38b5`  
		Last Modified: Thu, 02 Nov 2023 02:02:32 GMT  
		Size: 5.5 MB (5530319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c31d2fa6ab900de2558713a45dcc8b5204955dc606091f7ed7e0048330c107`  
		Last Modified: Thu, 02 Nov 2023 02:02:35 GMT  
		Size: 58.8 MB (58821329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fcecc41e97f107c64265e91d91f94a1ac6c9396edd04660b795f76da6069c294
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216487797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14aebee56a6a76606850f64aed55e4dcebb225baba563697ffe41f2c4f0184ce`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:21:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 03:28:09 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Thu, 02 Nov 2023 03:28:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 03:28:12 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 02 Nov 2023 03:28:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 03:28:12 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 03:28:18 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 02 Nov 2023 03:28:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 03:28:18 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 02 Nov 2023 03:28:36 GMT
RUN boot
# Thu, 02 Nov 2023 03:28:37 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a214d30cfffddc78d15882c23dbbb68b263dad08cc11c233ef134c0c7e821fd`  
		Last Modified: Thu, 02 Nov 2023 03:38:08 GMT  
		Size: 102.7 MB (102701531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f480439d9ac792573308f85fc3f1298471a11461b4bc3a2cf8637165870ba1`  
		Last Modified: Thu, 02 Nov 2023 03:38:02 GMT  
		Size: 5.4 MB (5353226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b20f83513c1093af5c1b11b5c792e2718bde2a743109ee31259be09586d299`  
		Last Modified: Thu, 02 Nov 2023 03:38:04 GMT  
		Size: 58.8 MB (58820387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
