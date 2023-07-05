## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:4eb96126b375a78811aff52c3f6178d6a50442cde33b8ea2759e968bef66bcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b826b517e5d7c9d36dac141d708e7dea5f0d160421bbdce2bfd100a6b3dbce2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289864844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea9185e35400532a55d3de9b642becc00b2a8261261edf6f86b78ecf5657005`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:00:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 11:19:30 GMT
COPY dir:3cd19417e6ca044e31be7ef3c49c7d24f962c0f648fd205b421373092856c87f in /opt/java/openjdk 
# Wed, 05 Jul 2023 11:19:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 11:19:32 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Jul 2023 11:19:32 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Jul 2023 11:19:32 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 11:19:37 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Jul 2023 11:19:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Jul 2023 11:19:37 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Jul 2023 11:19:55 GMT
RUN boot
# Wed, 05 Jul 2023 11:19:56 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099caecba99bf99b21cfbb7f1c23915fe48406202f54aa425cdb8d4341babebd`  
		Last Modified: Wed, 05 Jul 2023 11:32:56 GMT  
		Size: 198.5 MB (198549444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433fd9bcc0cf5238347c5e68dca7a3524729e24ffa19ae1aae946329d43d6bb3`  
		Last Modified: Wed, 05 Jul 2023 11:32:43 GMT  
		Size: 1.1 MB (1077515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708b6a13a082d7b3a43edc526df7ae92f0e32e81126b344f32aecad2652a4125`  
		Last Modified: Wed, 05 Jul 2023 11:32:46 GMT  
		Size: 58.8 MB (58820497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:873b9c31148f41a49245bdf5a310d72fac19e0aff1ee6f38c06381471e9fa33b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285272558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c98b215f6f8eac3c85e7fa79f93d260ea41e9f73ed75811ffffe52830032f2`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 03:35:40 GMT
COPY dir:46f070668c95bcfc449ea3e3aa03838e4c3f9939658e6aebe91ca179e673aded in /opt/java/openjdk 
# Wed, 05 Jul 2023 03:35:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 03:35:44 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Jul 2023 03:35:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Jul 2023 03:35:45 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 03:35:49 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Jul 2023 03:35:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Jul 2023 03:35:49 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Jul 2023 03:36:06 GMT
RUN boot
# Wed, 05 Jul 2023 03:36:07 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b90eb25a0fa4522274c461d519d4e554d5d39052358c321552f0848e5d55556`  
		Last Modified: Wed, 05 Jul 2023 03:46:58 GMT  
		Size: 195.3 MB (195324199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7caefa2cedf74bfb79fd843d222e0f4a346b362def6b567af103f940138169`  
		Last Modified: Wed, 05 Jul 2023 03:46:47 GMT  
		Size: 1.1 MB (1064819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477aa9cbad9751c4be76e06a3fe6ff99286e7f7a16155ea3a95e0a704455fab0`  
		Last Modified: Wed, 05 Jul 2023 03:46:50 GMT  
		Size: 58.8 MB (58820583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
