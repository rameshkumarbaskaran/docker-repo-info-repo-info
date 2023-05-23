## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:c74f5d98824213288f075528448aaecbff1a828bd48332d8af30f815a9e8a78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7b53ff9adf642170efdeeda95e4db6483384c40b2bbd8cfde7b8b7c9aa1746b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314780790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21e6d87ee422aff7b16e82be0c170cc1ca62157bbeedc041e2782ad959735a9`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 23 May 2023 01:20:00 GMT
ADD file:150a6453ab2258061c1a1549ab119df752bdc2c2c84028fa0e83a0663cd8cedf in / 
# Tue, 23 May 2023 01:20:01 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:04:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 08:07:13 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Tue, 23 May 2023 08:07:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:07:15 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 23 May 2023 08:07:15 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 23 May 2023 08:07:15 GMT
WORKDIR /tmp
# Tue, 23 May 2023 08:07:20 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 23 May 2023 08:07:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 23 May 2023 08:07:21 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 23 May 2023 08:07:39 GMT
RUN boot
# Tue, 23 May 2023 08:07:40 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bd73737482dd5575526c7207872963479808d979ab2741c321706b8553918474`  
		Last Modified: Tue, 23 May 2023 01:23:46 GMT  
		Size: 55.0 MB (55049027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a637a166556170916fb88fe2f41e4f73c2a4d05f0bd97e2366c20d1c5a96c1`  
		Last Modified: Tue, 23 May 2023 08:16:52 GMT  
		Size: 198.5 MB (198549521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfac14bea93f1fe71f5b4529c4f04c964e1c25d318e4b6bb03326517a922d2d6`  
		Last Modified: Tue, 23 May 2023 08:16:40 GMT  
		Size: 2.4 MB (2361685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1187687efc3ef2021f46ca2432a4c7337fdad17af474475b53ecc699d2b03b`  
		Last Modified: Tue, 23 May 2023 08:16:42 GMT  
		Size: 58.8 MB (58820557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f17a879ddf55c28fdf09b719cd8d2b7f1ebe6aeafab213ea1d0199498862f572
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310188429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef370a43f84214e1ff1a10fd8827d0afcd029ecd2d1756475684f19f9ccc588`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 23 May 2023 00:43:08 GMT
ADD file:a823391455122220a061ff349b66ee33413e968447ec5ba4bd544d9182fa2fbe in / 
# Tue, 23 May 2023 00:43:08 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:26:55 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Tue, 23 May 2023 01:27:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 01:27:00 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 23 May 2023 01:27:00 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 23 May 2023 01:27:00 GMT
WORKDIR /tmp
# Tue, 23 May 2023 01:27:04 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 23 May 2023 01:27:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 23 May 2023 01:27:05 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 23 May 2023 01:27:23 GMT
RUN boot
# Tue, 23 May 2023 01:27:23 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:b04fae59f135dd79280e4a6da39408e04c6d703c617cbcb1c524dfe6f2962fe5`  
		Last Modified: Tue, 23 May 2023 00:45:45 GMT  
		Size: 53.7 MB (53692612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e206de1cfcbe93e5295be6e8b68ac1878120e16eb1f6a6d4211f2d2a345f1fe`  
		Last Modified: Tue, 23 May 2023 01:35:30 GMT  
		Size: 195.3 MB (195324210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804226f8c0375eeda1223ccc8ba8c20433f8585e49ab0576f87fc575cee89474`  
		Last Modified: Tue, 23 May 2023 01:35:20 GMT  
		Size: 2.4 MB (2351050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6624e836eb681038457c128adac001b0b12465dc7599add77b50d2293d1d5576`  
		Last Modified: Tue, 23 May 2023 01:35:22 GMT  
		Size: 58.8 MB (58820557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
