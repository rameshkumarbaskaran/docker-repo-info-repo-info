## `clojure:temurin-8-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:31e3063943f06e406b0d11f89d65657ebed19ed62648f710c4a14bdbfa3578ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1809cc0e825d5ddbcbacea8fd5459b8e93d22943624b2a52130875c8dc869bb3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170864618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14d83c3ae8f7ccd80fdbc9cddfe812b6c43a29b6b9d3bbcb4eae4e8d4972832`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:05 GMT
ADD file:b03d13d345c29f69557f410c8504e748226756d1f48e5abdb63cd40179b2640c in / 
# Thu, 09 Feb 2023 03:20:05 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:22:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Feb 2023 09:22:06 GMT
COPY dir:bbb84183d7ea38d81d8401f01e29d08935ee4c8bf6f90c6527579a1554c3bde1 in /opt/java/openjdk 
# Thu, 09 Feb 2023 09:22:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 09:22:06 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 09 Feb 2023 09:22:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 09 Feb 2023 09:22:07 GMT
WORKDIR /tmp
# Thu, 09 Feb 2023 09:22:13 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 09 Feb 2023 09:22:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Feb 2023 09:22:13 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 09 Feb 2023 09:22:30 GMT
RUN boot
# Thu, 09 Feb 2023 09:22:31 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1e4aec178e0864db93a6f97a20bde3445871a4562c1801185eca1238d3a0e80d`  
		Last Modified: Thu, 09 Feb 2023 03:24:47 GMT  
		Size: 55.0 MB (55046771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002e7af6c4fa5dcefe0cea885d5bc9ca4379383c456abb3a1ebe2728ac33a5e7`  
		Last Modified: Thu, 09 Feb 2023 09:36:44 GMT  
		Size: 54.6 MB (54635546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11256390ab060b83cddfa7c32127256eefdf8a13fd16f7a07bafca272b498c2`  
		Last Modified: Thu, 09 Feb 2023 09:36:37 GMT  
		Size: 2.4 MB (2361729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c060d4c1ab427beb4e0d931b1f7821090f06e68b1cd40a888f8bcb542a7207`  
		Last Modified: Thu, 09 Feb 2023 09:36:41 GMT  
		Size: 58.8 MB (58820572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b9304542338b8459424bb495cb9ad116fad803d833dd7ee58946e7565c2d3086
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168602811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646bf220b20e25f3cf3a3534ab5c99690975b8576ff945bb5a12834fe834e8dc`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:01:16 GMT
COPY dir:b6d7e5613532d986930216de9e0fece0632e82564ce7a6a98baf63b4115f840d in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:01:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:01:17 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 03:01:17 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:01:17 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:01:22 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 03:01:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:01:23 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 03:01:55 GMT
RUN boot
# Wed, 01 Mar 2023 03:01:55 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b583ae59cedb3d06068194d612b2461bcf03fea5f1f8704c8a9987f693705b0a`  
		Last Modified: Wed, 01 Mar 2023 03:14:07 GMT  
		Size: 53.7 MB (53727940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d45d2418b64eeb2773490dc3776397fc0b7b7a6edd7aee96b720a9d29e4c8e`  
		Last Modified: Wed, 01 Mar 2023 03:14:02 GMT  
		Size: 2.4 MB (2350919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336b623dcf2b05cc69746e8ace440c8fd27ce65367f12dd186e23d2af3f3f14e`  
		Last Modified: Wed, 01 Mar 2023 03:14:04 GMT  
		Size: 58.8 MB (58820737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
