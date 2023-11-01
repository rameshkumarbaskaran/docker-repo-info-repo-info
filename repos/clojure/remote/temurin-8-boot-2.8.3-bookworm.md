## `clojure:temurin-8-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:1194bf89f81fdca24ff27d83a009630b18d5972525f906f47094a8d192fa8b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2e71ae371def284ded8b756ee5734ebc47f22639400e28cf1cdbb767801404ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217518499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f015386276cefca320ec6c94dad5cf8c9e1ad84faf1d5d6ed751496afca3ff19`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:10:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:11:36 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:11:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:11:37 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:11:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:11:37 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:11:43 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:11:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:11:43 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:12:29 GMT
RUN boot
# Wed, 01 Nov 2023 01:12:30 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e319efa3c1ccba3860787f9c73906b26268d4cfba0f893ba6660f2ff59cdf0`  
		Last Modified: Wed, 01 Nov 2023 01:32:58 GMT  
		Size: 103.6 MB (103585059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794fd1cf14ddbb724ddf76b0f65dc0023bbb40c6122749bc60eaf29a2eb400d7`  
		Last Modified: Wed, 01 Nov 2023 01:32:51 GMT  
		Size: 5.5 MB (5530340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3475fe277c96e19a4c639a8a998e877ab05f8d8838a88e6fe7a715208b49f`  
		Last Modified: Wed, 01 Nov 2023 01:32:53 GMT  
		Size: 58.8 MB (58821076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f378f4c570196b338382eac6eaaf142722ef9b676d5b577c7874520fb4c40b4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216476956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0083a1089489df1f8df6b28e77785bcc2b17cb6c40fa2e2bce6b571a0071314e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:32 GMT
ADD file:c934ceb4c53a1cce6779198f1ea73d5c8aad9a035e750b343d49826120ecd0eb in / 
# Wed, 01 Nov 2023 00:39:33 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:21:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 02:21:50 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 01 Nov 2023 02:21:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:21:52 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 02:21:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 02:21:52 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 02:21:58 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 02:21:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 02:21:58 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 02:22:16 GMT
RUN boot
# Wed, 01 Nov 2023 02:22:16 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8024d4fb53b2455f66d49b7ee72eb3cad5074043578238b796a9879955946a88`  
		Last Modified: Wed, 01 Nov 2023 00:42:44 GMT  
		Size: 49.6 MB (49612653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fccb7d2235ea2a72ac31188f98768da3ba53d7b513fc150bf335e52018597db0`  
		Last Modified: Wed, 01 Nov 2023 02:41:02 GMT  
		Size: 102.7 MB (102690512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c22457774f8d604fbadcaebebb9cf34a52c75b1b43862a79e38bf74812777a`  
		Last Modified: Wed, 01 Nov 2023 02:40:55 GMT  
		Size: 5.4 MB (5353286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820c04354ed79a21336f3a977adc5e9ae87b35f1e999373a9a081ec1d9dd40bf`  
		Last Modified: Wed, 01 Nov 2023 02:40:57 GMT  
		Size: 58.8 MB (58820505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
