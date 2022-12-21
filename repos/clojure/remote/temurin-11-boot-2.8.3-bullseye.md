## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:7c844be8b4af612623e65aedb0f71c15c802ea6186e920d414975d6fb0f8e276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5726c90f3784edf609c31865ad35fb9f8ce935746bc20f733d870e1a9d581214
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314661084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a287aae45894a907a37e2e6060cb60d71fccbd854d93b67829c7663df6acfd20`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:21 GMT
ADD file:c13b430c8699df107ffd9ea5230b92238bc037a8e1cbbe35d6ab664941d575da in / 
# Wed, 21 Dec 2022 01:20:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:50:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 21 Dec 2022 01:53:31 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 21 Dec 2022 01:53:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 01:53:32 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 21 Dec 2022 01:53:32 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 21 Dec 2022 01:53:33 GMT
WORKDIR /tmp
# Wed, 21 Dec 2022 01:53:38 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 21 Dec 2022 01:53:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 21 Dec 2022 01:53:39 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 21 Dec 2022 01:53:57 GMT
RUN boot
# Wed, 21 Dec 2022 01:53:57 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:32de3c850997ce03b6ff4ae8fb00b34b9d7d7f9a35bfcdb8538e22cc7b77c29d`  
		Last Modified: Wed, 21 Dec 2022 01:24:10 GMT  
		Size: 55.0 MB (55025166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09879893307507e7fe968e99bda720fc4263e5da6b74edf0064ca1f992ab9605`  
		Last Modified: Wed, 21 Dec 2022 02:06:55 GMT  
		Size: 198.5 MB (198454573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40919b3b9da0bda0e8aef511927e9e2a2fbb0b81559ec8887f8f142409c73825`  
		Last Modified: Wed, 21 Dec 2022 02:06:41 GMT  
		Size: 2.4 MB (2360765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91978998a5b59a7615b6848be8262477c4b52c48533797affbe91c0a40cf8290`  
		Last Modified: Wed, 21 Dec 2022 02:06:44 GMT  
		Size: 58.8 MB (58820580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3bdbe312d9116a10153df30f0e6c99f4e3aaf99042dd77319be56306fdcc9ca1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310075334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f507ef80166a28e856fc45420f35a915f760e77de0c0f382b81ca0b13420af`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:06 GMT
ADD file:b1e7652678bbfc9556636e77d79c947ff1436888e2929f9c5c3ddb42a50c1176 in / 
# Tue, 06 Dec 2022 01:40:07 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 05:03:32 GMT
COPY dir:e387a3b68139ff88bdac27d5ce097fc680f3cae9fdd88c28cdd91a06f9205180 in /opt/java/openjdk 
# Fri, 09 Dec 2022 05:03:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 05:03:36 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 09 Dec 2022 05:03:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 09 Dec 2022 05:03:36 GMT
WORKDIR /tmp
# Fri, 09 Dec 2022 05:03:42 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 09 Dec 2022 05:03:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 09 Dec 2022 05:03:42 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 09 Dec 2022 05:04:00 GMT
RUN boot
# Fri, 09 Dec 2022 05:04:00 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:4948a51a9a3f176f30ac619014f4a2da453a943244eacb53096ee9742eb7cef1`  
		Last Modified: Tue, 06 Dec 2022 01:43:33 GMT  
		Size: 53.7 MB (53699146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1dc93c936f130a0b32765e5801ad37ff3679f9461520ae91ce9b6fa4d65888`  
		Last Modified: Fri, 09 Dec 2022 05:18:13 GMT  
		Size: 195.2 MB (195203416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e219abf9fbea314537b995be27f2a4efc9a3d2cf850832fc4947aa9dd118af0`  
		Last Modified: Fri, 09 Dec 2022 05:18:02 GMT  
		Size: 2.4 MB (2352310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be250b89bf6b3fb89b52f7b2c55af8056e8ac0491e4cae409df0f8018619f1f1`  
		Last Modified: Fri, 09 Dec 2022 05:18:04 GMT  
		Size: 58.8 MB (58820462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
