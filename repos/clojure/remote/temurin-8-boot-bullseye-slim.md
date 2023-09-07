## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:ec540d72b73b62fefc8545232754040dcfabe8a17df3eee3338992e20af05b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:01e29bf61f57914e5802004ed62b4c92d9d609cb2f7aee2d7e84f99985b18b06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194900634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb52bb4f2f5ea99c10030bd3b7abb2c748cb491a621a83899c95c196794c7846`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:03:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 03:18:35 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Thu, 07 Sep 2023 03:18:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 03:18:36 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 07 Sep 2023 03:18:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 03:18:36 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 03:18:42 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 07 Sep 2023 03:18:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 03:18:42 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 07 Sep 2023 03:19:01 GMT
RUN boot
# Thu, 07 Sep 2023 03:19:01 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a386eaaac993939aefc9356b5f6cc0468dd852762a0b7bb3e195a40c8caf53b`  
		Last Modified: Thu, 07 Sep 2023 03:29:54 GMT  
		Size: 103.6 MB (103585038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f1cade318a18d69d2e48da87953688c38e0007607f1593cc887d404fad90fd`  
		Last Modified: Thu, 07 Sep 2023 03:29:45 GMT  
		Size: 1.1 MB (1077566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76c78ce5194c7ff74e2fb2ecd89f78b1e9b098c3b1821a76993ee18d14367c9`  
		Last Modified: Thu, 07 Sep 2023 03:29:48 GMT  
		Size: 58.8 MB (58820527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0d0736b04bee60be5a08e210df3cae675b2b5d63363e4619ef3fe11798304cf9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192638622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc2957c07bdf1640fbe1078ffde1ac79edb1a5488248e1ef52f6e10bb1eb695`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 01:46:48 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 16 Aug 2023 01:46:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 01:46:51 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 16 Aug 2023 01:46:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 01:46:51 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 01:46:55 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 16 Aug 2023 01:46:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 01:46:55 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 16 Aug 2023 01:47:13 GMT
RUN boot
# Wed, 16 Aug 2023 01:47:13 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab72539caee6a49c911d508260d1eb9ece05d94c06a86d77b415da3e7508716b`  
		Last Modified: Wed, 16 Aug 2023 01:56:31 GMT  
		Size: 102.7 MB (102690456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f12b45221626ad8753f0a6ebace7913cc4f42edd901d45d774395d3769c8a6`  
		Last Modified: Wed, 16 Aug 2023 01:56:24 GMT  
		Size: 1.1 MB (1064823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8caee25463fc6e0f73ccc69a600b422e99c42a711c6884d04bd23dd45b261a9f`  
		Last Modified: Wed, 16 Aug 2023 01:56:27 GMT  
		Size: 58.8 MB (58820527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
