## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:e994f5e4429775db38fd37579910011a4671ea678c0d6080b8efdccf2d2d6ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:50a30066f3367ddf314dd873ddb436666f0d4c4613d53554d506ad44a04b39e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314682007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a1ecd5d6b21087910f359213c1de7585e3da9ef5b34ee4c0616d38c5a0097e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:29 GMT
ADD file:917750a82b29f8f7f88a121017bd9dfeb0fbcc8f0697a009f08b6b58246eff4b in / 
# Wed, 11 Jan 2023 02:34:30 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:18:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Feb 2023 03:12:07 GMT
COPY dir:fdbc5e9dec2946fa124877176e92a68dd3fe3a70def5bb906a6040c4a1303a2d in /opt/java/openjdk 
# Wed, 01 Feb 2023 03:12:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Feb 2023 03:12:09 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Feb 2023 03:12:09 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Feb 2023 03:12:09 GMT
WORKDIR /tmp
# Wed, 01 Feb 2023 03:12:17 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Feb 2023 03:12:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Feb 2023 03:12:17 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Feb 2023 03:12:36 GMT
RUN boot
# Wed, 01 Feb 2023 03:12:36 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bbeef03cda1f5d6c9e20c310c1c91382a6b0a1a2501c3436b28152f13896f082`  
		Last Modified: Wed, 11 Jan 2023 02:38:42 GMT  
		Size: 55.0 MB (55025206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d363760f28bab547ae93a2be40d06ddf28eb305931fd24296747ab14617efc3`  
		Last Modified: Wed, 01 Feb 2023 03:30:18 GMT  
		Size: 198.5 MB (198475543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a44e5f2b1b372aa1d46c7e66cc318aa9a6a8b4bf84d2ed2897a3dfa3e51c147`  
		Last Modified: Wed, 01 Feb 2023 03:30:03 GMT  
		Size: 2.4 MB (2360813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a35cf2f5309d621ca9e708575d3c2e9b1d8e79bed18d46d6e9ba3802566baed`  
		Last Modified: Wed, 01 Feb 2023 03:30:06 GMT  
		Size: 58.8 MB (58820445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d45db6393d0db9a02767fb1f147d79504bd24a26ec74495980ec0e9ff541533e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310093471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62b49ff3f5b0c04e400780990ef221cd0a655e5442f9975691e64ce1b096bd1`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:24 GMT
ADD file:9e185c2d9ca8a231a39ee2b1761fcdff75065252d25a65a207acb7a319c1cf23 in / 
# Wed, 11 Jan 2023 02:57:25 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 20:49:40 GMT
COPY dir:b661686bf8d434588756c45f2ef6e7f314f32f753cf180ef8fb45397388f098c in /opt/java/openjdk 
# Tue, 31 Jan 2023 20:49:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 20:49:44 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Jan 2023 20:49:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Jan 2023 20:49:44 GMT
WORKDIR /tmp
# Tue, 31 Jan 2023 20:49:50 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Jan 2023 20:49:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Jan 2023 20:49:50 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Jan 2023 20:50:07 GMT
RUN boot
# Tue, 31 Jan 2023 20:50:07 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c345c9e441f5f49235768af74b8ab37743652d38958afaa000edd56d7b2f0540`  
		Last Modified: Wed, 11 Jan 2023 03:00:56 GMT  
		Size: 53.7 MB (53681859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4582f4343bacf57f66f8e6afa3b09983b023babf5d4da2ccacfead5d1e72571`  
		Last Modified: Tue, 31 Jan 2023 21:04:14 GMT  
		Size: 195.2 MB (195240378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464d7f147fe6f8e84004a3d3d926b3f8a2614678054a0c29e95c3b764b9288da`  
		Last Modified: Tue, 31 Jan 2023 21:04:03 GMT  
		Size: 2.4 MB (2350668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ace99a37b6a1b9f545ba77a0392ba0914c997be05f5b82f567b92ad09d1c03f`  
		Last Modified: Tue, 31 Jan 2023 21:04:06 GMT  
		Size: 58.8 MB (58820566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
