## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:a498f67c85725c38c148e77e897d743d9f8fd71eeb44e4615f6611b202221c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:84e80a04d6eeaad5d58fd25a9107e9e9952611701fb09585688cd0903505e856
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289850871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8a6508393dae7c0178b0a498c4515a5be1ae194b47047f4fbbab92c2488562`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 20:27:22 GMT
COPY dir:df592a42a629b9630bdf0ab57a63e6c60f66d91934439985e01efbb58723e9ee in /opt/java/openjdk 
# Wed, 03 May 2023 20:27:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:27:24 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 May 2023 20:27:24 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 May 2023 20:27:24 GMT
WORKDIR /tmp
# Wed, 03 May 2023 20:27:29 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 03 May 2023 20:27:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 May 2023 20:27:29 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 May 2023 20:27:46 GMT
RUN boot
# Wed, 03 May 2023 20:27:47 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0ff29d68fcfaa0b79ea63e544be12bffb5a83bf5c3d7b0d8ce3ccbdc611171`  
		Last Modified: Wed, 03 May 2023 20:36:57 GMT  
		Size: 198.5 MB (198549520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2747774d6540f4ab5b6c172b641d91418ffae239fd51ae0eac24039e00daec24`  
		Last Modified: Wed, 03 May 2023 20:36:44 GMT  
		Size: 1.1 MB (1077538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf326ee31dcfce9e51555c636c3366bb656a8e5f66d6084bfafc44c42f8124d0`  
		Last Modified: Wed, 03 May 2023 20:36:47 GMT  
		Size: 58.8 MB (58820297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:852cb6dc896fd292844e2d9718d3c63eb88479c7be0437bc9ede503d440877ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285262105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437fdcf21262be80eefe79324f429a1fe5bfaa373b39e8095a3483eb5c81e74b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:10:37 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Thu, 04 May 2023 10:10:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 10:10:42 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 04 May 2023 10:10:42 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 04 May 2023 10:10:42 GMT
WORKDIR /tmp
# Thu, 04 May 2023 10:10:47 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 04 May 2023 10:10:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 04 May 2023 10:10:47 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 04 May 2023 10:11:03 GMT
RUN boot
# Thu, 04 May 2023 10:11:03 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8372f00ab12bb739ea85b3b21db2dbe4809c7c3bd11102276ddbe52e3a864e`  
		Last Modified: Thu, 04 May 2023 10:20:09 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef59295312d5d90cbd500717868d9b3d0a6d7ed6ba8f522190c0fb2865b0cbd1`  
		Last Modified: Thu, 04 May 2023 10:19:58 GMT  
		Size: 1.1 MB (1064812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e6ac463a6ddd6ae6de5f03afff6f8cf617825d997748401592b051a2715af3`  
		Last Modified: Thu, 04 May 2023 10:20:00 GMT  
		Size: 58.8 MB (58820351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
