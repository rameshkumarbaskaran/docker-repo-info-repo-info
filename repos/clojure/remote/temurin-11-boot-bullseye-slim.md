## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:34d3a83a157a3660f3021f06e35409c88be745e05d81ea557552c039e7e19a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:521e5c1db50b9441ff3b617288391c5b9074c867d075c688da6c688398fb0ef9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289444309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0052360c76d093610af901491922388724e1b6aaa90e0d1ca2a948fe10c56a1b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:11:14 GMT
COPY dir:24028fba84faa85b57bc32be14abf8fad6a4bd4db557cb5499b6d5cf38d97646 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:11:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:11:16 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Nov 2022 20:11:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Nov 2022 20:11:16 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:11:22 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 02 Nov 2022 20:11:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Nov 2022 20:11:22 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Nov 2022 20:11:43 GMT
RUN boot
# Wed, 02 Nov 2022 20:11:43 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9424e0e92a9d7ac25f2f902e3550e25f0379d53b383d802d0c0a9174fddd9e5d`  
		Last Modified: Wed, 02 Nov 2022 20:24:52 GMT  
		Size: 198.1 MB (198124751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbff5570796254114924dd02d5f8946adca8cab668cd9e7cc7d84c73b3f933d`  
		Last Modified: Wed, 02 Nov 2022 20:24:37 GMT  
		Size: 1.1 MB (1079015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162b1b64d17ba5b9df1a2d439cdeb0173c756ce54bdba5d0133a065a559d336b`  
		Last Modified: Wed, 02 Nov 2022 20:24:41 GMT  
		Size: 58.8 MB (58820505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5170f6df383f48f77776b6ada3321b9a72eb399486347bc9f2774e723e5a2fda
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284818291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780ef279586baf7b8307a20fe5f1976f0429ad2fcf03b5f4d6e86fd6973b0b04`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:47:12 GMT
COPY dir:e48336735658172388295f760b71f5f10a9b7d3f960c6e4546718a38dd6452e7 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:47:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:47:16 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Nov 2022 20:47:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Nov 2022 20:47:16 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:47:21 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 02 Nov 2022 20:47:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Nov 2022 20:47:21 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Nov 2022 20:47:38 GMT
RUN boot
# Wed, 02 Nov 2022 20:47:38 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc966be4bd15170671412b817450394760b037c8e5e3587768bfc3bbd123d53`  
		Last Modified: Wed, 02 Nov 2022 20:58:36 GMT  
		Size: 194.9 MB (194867681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d77995ba52e41179dd6ff3b487a05dbaac2d72b42e16ccaaea406a2d17de94a`  
		Last Modified: Wed, 02 Nov 2022 20:58:25 GMT  
		Size: 1.1 MB (1066353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf94edc076360bc715c4325bebea2f50951bb9c7c4240bf9e99db8166c877d0`  
		Last Modified: Wed, 02 Nov 2022 20:58:27 GMT  
		Size: 58.8 MB (58820347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
