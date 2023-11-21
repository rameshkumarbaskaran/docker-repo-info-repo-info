## `clojure:temurin-8-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:bb30be4a82004f541a958e289ebf7cda9482f9b95fb2aa6e92c4512a0fecc0e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:127c6e7fa462a42a6461070571c422c13cd60d2d8fd381d6903f144700c52489
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219845339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6e770d8f6864121595fcc4c431d5b866e1577caa231e2b9983549b6cc48caa`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:59 GMT
ADD file:da3938f00f114fa8f5948fb7182da39c43e5ce57a334ba528681cb29aff0d2f6 in / 
# Wed, 01 Nov 2023 00:21:00 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Nov 2023 01:51:00 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 02 Nov 2023 01:51:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 01:51:00 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 02 Nov 2023 01:51:00 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 02 Nov 2023 01:51:00 GMT
WORKDIR /tmp
# Thu, 02 Nov 2023 01:51:07 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 02 Nov 2023 01:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 Nov 2023 01:51:07 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 02 Nov 2023 01:51:25 GMT
RUN boot
# Thu, 02 Nov 2023 01:51:26 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2f088d622efd8dbaa13d01eafd0aac8f9f33bb335edd3be897ae8059338c7bf7`  
		Last Modified: Wed, 01 Nov 2023 00:25:49 GMT  
		Size: 55.1 MB (55058052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ae3bc407ed44ee4c19e2acfaafba1a8237df1bc1f1bca7853c10d12070957d`  
		Last Modified: Thu, 02 Nov 2023 02:03:16 GMT  
		Size: 103.6 MB (103598251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0179f72fd84b50b99e6cb97f31a09b9531caadde016ceab0d33ebef3b876a28d`  
		Last Modified: Thu, 02 Nov 2023 02:03:08 GMT  
		Size: 2.4 MB (2368697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0711c4965ec79bd328e0ef4d22bdc61956ffea6375e1e45849c2e53e1e6d83e0`  
		Last Modified: Thu, 02 Nov 2023 02:03:11 GMT  
		Size: 58.8 MB (58820339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; arm64 variant v8

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
