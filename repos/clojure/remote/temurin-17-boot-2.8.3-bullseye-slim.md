## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:13beda18286e6b688a1720a011af0463e5493d460060786676fe5ec9fd40b930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:65e8471228fad768702754fa76c98c19d133a4103a1b6bcb0555873c6d79aae9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283733488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f428670d05c0b1dc82a6289c581e31fb344af88d30be2d53f3fa082529133f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Feb 2023 03:18:17 GMT
COPY dir:5cf52f938fe415b0022fbccb8cf978562c503c0b8313cc9dedf46c1c4edb35cf in /opt/java/openjdk 
# Wed, 01 Feb 2023 03:18:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Feb 2023 03:18:19 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Feb 2023 03:18:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Feb 2023 03:18:19 GMT
WORKDIR /tmp
# Wed, 01 Feb 2023 03:18:24 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Feb 2023 03:18:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Feb 2023 03:18:25 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Feb 2023 03:18:46 GMT
RUN boot
# Wed, 01 Feb 2023 03:18:47 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Feb 2023 03:18:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Feb 2023 03:18:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd5222c39363e9ad4cf3befb9bb980d24da88c73d38324ec54e4613c745a424`  
		Last Modified: Wed, 01 Feb 2023 03:33:57 GMT  
		Size: 192.4 MB (192438216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59854c1ad16f87275762c109bd5b566ec6c33e9f75cb65ad80225eef4c0c6ce1`  
		Last Modified: Wed, 01 Feb 2023 03:33:43 GMT  
		Size: 1.1 MB (1077329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14010e2293680c5d3004caef4c590962e9d0b4ecf8c678df4f649a22205721cb`  
		Last Modified: Wed, 01 Feb 2023 03:33:46 GMT  
		Size: 58.8 MB (58820570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3cc80209f35dc0ca07888b0b7f5fb36875ece80c871d2065785de77c88d053`  
		Last Modified: Wed, 01 Feb 2023 03:33:43 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c2c0777c20438ba512acc89687f26734efaf73733253ad1dcc76ed36e5423a64
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281190760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95f17722a1402178d1c00d6b8a6284c9f220c22eb7b44c20513f301f8d586b2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Jan 2023 20:54:33 GMT
COPY dir:a1bd99c3d82513db94430c73467e1e5c69ea4624d0489571d594afe503e15dc5 in /opt/java/openjdk 
# Tue, 31 Jan 2023 20:54:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 20:54:37 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Jan 2023 20:54:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Jan 2023 20:54:38 GMT
WORKDIR /tmp
# Tue, 31 Jan 2023 20:54:42 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Jan 2023 20:54:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Jan 2023 20:54:42 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Jan 2023 20:54:58 GMT
RUN boot
# Tue, 31 Jan 2023 20:54:59 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 31 Jan 2023 20:54:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 31 Jan 2023 20:54:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a105a97fdf20185e2d7c3fa185a80f146fc82f987de1e73befa061b450f1bf`  
		Last Modified: Tue, 31 Jan 2023 21:07:37 GMT  
		Size: 191.3 MB (191260408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10599be03ab26522c705999f0984ab5e2c0017502823e3151b33737b897ea15`  
		Last Modified: Tue, 31 Jan 2023 21:07:24 GMT  
		Size: 1.1 MB (1064686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c692dad51513751c689629f478ec8545597f92c2c523d8a691cdd05a4f30645b`  
		Last Modified: Tue, 31 Jan 2023 21:07:27 GMT  
		Size: 58.8 MB (58820454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf67f460b0deeb2d91107e6c7be60f9b5c9720dd4be4b33461cc05a71571efb5`  
		Last Modified: Tue, 31 Jan 2023 21:07:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
