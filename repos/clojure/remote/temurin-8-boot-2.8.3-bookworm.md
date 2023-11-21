## `clojure:temurin-8-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:cf433fc5580b5d7c36a5e1ad2cd8505115b70278018b0097d75275fbd9cd44f6
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
$ docker pull clojure@sha256:1cc26b2aaff582104f1ed35599f8f57a4de38bfa342fd04fe06976bea9333c5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216488398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3993b92364dcda172bfd11746f90de489c7d0a4449e1fbe25d2bd7c4aa7276b7`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:21:05 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:21:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 07:21:08 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 07:21:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 07:21:08 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 07:21:13 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 07:21:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 07:21:13 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 07:21:53 GMT
RUN boot
# Tue, 21 Nov 2023 07:21:53 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed78b2f6a939d9bf427c5f2e807ccac60d5947b296d683ccf2519fb74ff8df3`  
		Last Modified: Tue, 21 Nov 2023 07:39:58 GMT  
		Size: 102.7 MB (102701523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5801418b9463854fff767e3e912c934e0e74821a16d5916df5b25c3071145e1a`  
		Last Modified: Tue, 21 Nov 2023 07:39:52 GMT  
		Size: 5.4 MB (5353260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7878260d5fac855ccea4895264d7b8408656651a1bd8dbbfe8b3375e5058ed`  
		Last Modified: Tue, 21 Nov 2023 07:39:54 GMT  
		Size: 58.8 MB (58820965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
