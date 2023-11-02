## `clojure:temurin-8-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:f50c69de07fc3a310c71e20febd6bc88662757d002b8697b45df8fcecf97d545
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
