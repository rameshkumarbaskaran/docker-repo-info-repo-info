## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:053f845e0642246977a2392d02e98b829632e4cb11b24759aa1800620010082c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:206ab170afc3bcbedc9b09f33b1f0cbbdf548869731f455400c7932cb4084619
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.4 MB (308366852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6eb5e84ebdb0ed003fa50029eb2153595154af4efce2e807bf1215ca591a0ac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Oct 2022 02:39:23 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Tue, 25 Oct 2022 02:39:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 02:39:24 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 25 Oct 2022 02:39:25 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 25 Oct 2022 02:39:25 GMT
WORKDIR /tmp
# Tue, 25 Oct 2022 02:39:31 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 25 Oct 2022 02:39:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 25 Oct 2022 02:39:31 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 25 Oct 2022 02:39:51 GMT
RUN boot
# Tue, 25 Oct 2022 02:39:51 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 25 Oct 2022 02:39:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 25 Oct 2022 02:39:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac76dde2c2f13d28db088f654035acb0c8244b4c9447b8e9b0cfdb280fee3c55`  
		Last Modified: Tue, 25 Oct 2022 02:52:04 GMT  
		Size: 192.1 MB (192137591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b634bbf12e96ba68daf84945435fe526a086f43553876baf48e5af3c163acaf6`  
		Last Modified: Tue, 25 Oct 2022 02:51:50 GMT  
		Size: 2.4 MB (2362126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbdd9bb7939290f1b09a202ddc545ea2725af3f38293de94c3a0e947a2502eb`  
		Last Modified: Tue, 25 Oct 2022 02:51:53 GMT  
		Size: 58.8 MB (58820405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bf53b921ad1cc4e71562568ffb4b60e902379b64cf95a468d5fd1c2f917c56`  
		Last Modified: Tue, 25 Oct 2022 02:51:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1c330fa7707749f016e4dd0f57d37108a6951e8f5feaf4cb71d61d3066cf3003
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305565854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d88df19f31445ddd2508c7a51e2d61e243a190680c999c8970d1b8cc638e603`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:38:34 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Thu, 06 Oct 2022 02:38:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 02:38:35 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 06 Oct 2022 02:38:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 02:38:37 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:38:43 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 06 Oct 2022 02:38:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 02:38:45 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 06 Oct 2022 02:39:33 GMT
RUN boot
# Thu, 06 Oct 2022 02:39:35 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 02:39:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 02:39:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b7798e9e43d2494af502b188de7bd161f67c7162a0b931a6e81e4e8d7c52d5`  
		Last Modified: Thu, 06 Oct 2022 03:01:09 GMT  
		Size: 190.9 MB (190904332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4ef412f00089f24b2edfc91068b2b7fb2abd52a500ecf9af694d54dfd33ca0`  
		Last Modified: Thu, 06 Oct 2022 03:00:53 GMT  
		Size: 2.1 MB (2144374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347d5a654856778a35001fcc471f22bed20431af15eb7ff73479937eece2bf86`  
		Last Modified: Thu, 06 Oct 2022 03:00:58 GMT  
		Size: 58.8 MB (58816124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc1af18a1013bb03aa53e4ab2657b977d2681f2ab9b44a4aebe4796d90eac21`  
		Last Modified: Thu, 06 Oct 2022 03:00:52 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
