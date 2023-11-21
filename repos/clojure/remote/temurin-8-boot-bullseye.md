## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:7d94aeb181ca9a68465ca80a2070ab13d91d2ad231af99bc5c110f7e45663269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1dc64c00701fdafca4ec59d281e62780fe258a4abc9191e8b36070ddd6c4da79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219845201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97da5bcc8fd0d3b57788af2b44b0ca1482da41506e2ca93481d34bc023fb2e8`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:09:29 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Tue, 21 Nov 2023 10:09:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 10:09:30 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 10:09:30 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 10:09:30 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 10:09:35 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 10:09:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 10:09:35 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 10:09:54 GMT
RUN boot
# Tue, 21 Nov 2023 10:09:54 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340733a9bc147bdf73521b84a2d2eafba8cb7462c33ec7e8d6c8e63126915d10`  
		Last Modified: Tue, 21 Nov 2023 10:29:19 GMT  
		Size: 103.6 MB (103598259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9319fe661a759f8bd86de6f09550b2ff650eca9c8e341693d2dd107ed3ea4e2c`  
		Last Modified: Tue, 21 Nov 2023 10:29:10 GMT  
		Size: 2.4 MB (2368665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93ded59db4a8c7bf1f3baf372e6f57f44d431d059389acc8aa6f929335eced6`  
		Last Modified: Tue, 21 Nov 2023 10:29:13 GMT  
		Size: 58.8 MB (58820374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:faaa5a90ecc20fa5fbc4be474f68ae1c816defbf85457a19d867019bb68d2c4c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217587519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2c491cea50b8096521bbd5af47ef039adf64ef7812a9883884dcb4932cc673`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:22:30 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 07:22:32 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 07:22:32 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 07:22:32 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 07:22:38 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 07:22:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 07:22:38 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 07:22:55 GMT
RUN boot
# Tue, 21 Nov 2023 07:22:55 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368154bbc0c28d6812f708f5f6016f9d10e7e9305ac7fd1cdd4a216a6df5fd55`  
		Last Modified: Tue, 21 Nov 2023 07:40:29 GMT  
		Size: 102.7 MB (102701584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcaae535d7e63da4445c92c7a009b5c2ec78da8bc2322db46d3ccbc50064958b`  
		Last Modified: Tue, 21 Nov 2023 07:40:23 GMT  
		Size: 2.4 MB (2357441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55abbef8e7a658256c96041526ae0a7fcf125789bb8f23f36f7390ea34d41926`  
		Last Modified: Tue, 21 Nov 2023 07:40:25 GMT  
		Size: 58.8 MB (58820622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
