## `clojure:temurin-11-boot-bookworm`

```console
$ docker pull clojure@sha256:464fd38abeb78f9aedbc12c879d10df7d839cfc7cb7edc708251444d19162598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d825f8da6938824f341ceac89f9e3f3e302dd4a76c1a9134ea097968f747ec8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259199586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f059ad89fe5fb4f48f4f3ba99b7193ea0bda749a08f7c1c457447a329bf59d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:07:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:13:41 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 21 Nov 2023 10:13:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 10:13:42 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 10:13:42 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 10:13:42 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 10:13:48 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 10:13:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 10:13:48 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 10:14:05 GMT
RUN boot
# Tue, 21 Nov 2023 10:14:05 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9e2ffce8b869cca4ab630c3d07ac20aef995e43238cf9b53a85805a1ce76cc`  
		Last Modified: Tue, 21 Nov 2023 10:31:55 GMT  
		Size: 145.3 MB (145266641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d98e033318ecb0baecd3faa24d8b948b073ed25b073b0cf5a4d1fb70542671`  
		Last Modified: Tue, 21 Nov 2023 10:31:44 GMT  
		Size: 5.5 MB (5530327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d35d76f3452a87f197aa1299d96ceb59d008e404e58e92ebdee35fae602a926`  
		Last Modified: Tue, 21 Nov 2023 10:31:47 GMT  
		Size: 58.8 MB (58820393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:37866811476c0c9d0fcdcb0ec0c19cc005e2ef80fbc5bf0654801a05bb00900e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255788142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4217de0df9447c7d0e8aeefffef3bc1d0702b0cf3f06fe81636e77811c748b88`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:26:16 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:26:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 07:26:19 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 07:26:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 07:26:20 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 07:26:25 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 07:26:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 07:26:25 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 07:26:42 GMT
RUN boot
# Tue, 21 Nov 2023 07:26:42 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354d327993bf126405e169db138848ddbbe9f7b0434cc3fbc3132a2dafcb3ed1`  
		Last Modified: Tue, 21 Nov 2023 07:43:01 GMT  
		Size: 142.0 MB (142001937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be0125d46d180a3603fd23a37a8221e66e907958cd5d4cfad68b5e03efc11f3`  
		Last Modified: Tue, 21 Nov 2023 07:42:53 GMT  
		Size: 5.4 MB (5353207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32011ac7d4214e71c27fe34d41d7bd6cc74e12b7af98aa8bbc83393bc426463`  
		Last Modified: Tue, 21 Nov 2023 07:42:55 GMT  
		Size: 58.8 MB (58820348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
