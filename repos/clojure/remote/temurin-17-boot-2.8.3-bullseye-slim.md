## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:5dcd8719673cc09fe5d8699b4343b340ce5b5b6ba7c94e22c0271e512e2ac196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3db33d1e93c86a58cf935c022f93aa748c32597582674415d85323f03c9a5f83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236091917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb50838403e9ac6b18c9d74eadcd60f3e1a883731b8fe8537a7bc63540b659c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:44:13 GMT
COPY dir:762e280751e9eaacf2bfae42d6a8cb2a49846426bd7c5675b21a4c0c8ae8fb71 in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:44:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:44:15 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 03 Oct 2023 08:44:15 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 03 Oct 2023 08:44:15 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:44:20 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 03 Oct 2023 08:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Oct 2023 08:44:20 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 03 Oct 2023 08:44:38 GMT
RUN boot
# Tue, 03 Oct 2023 08:44:38 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 03 Oct 2023 08:44:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Oct 2023 08:44:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0567cd6aa99e5db3b54cc244cfee493561efcb8009ca2dc2c87b8c882d0bd562`  
		Last Modified: Tue, 03 Oct 2023 08:56:51 GMT  
		Size: 144.8 MB (144775742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0255256a56858e8069d0bd185968fe3c3efa36a706724551538a8a1e8f2dc643`  
		Last Modified: Tue, 03 Oct 2023 08:56:40 GMT  
		Size: 1.1 MB (1077528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d643f0fa2c38f573ffe102897ba26eade919e80b9fbb470759d2d1da94f830a`  
		Last Modified: Tue, 03 Oct 2023 08:56:44 GMT  
		Size: 58.8 MB (58820536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996243702f6b7ce75490cac3978616f509d977ee54e845761b78743e0d258380`  
		Last Modified: Tue, 03 Oct 2023 08:56:40 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:04ea87be2fbf4a9d92aeb8aa5b819a43f6a89d4e31dd3b34e5d65dd48f4e4f64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233491986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9f94ec6d12887b36cda1f7633ad58ba2bcd40d818902358d58f8622feb1425`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:48:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:32:36 GMT
COPY dir:9add47918f86acac35c907520d4811042633ac78a65fb2fbf0acc7586100f57a in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:32:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:32:40 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 03 Oct 2023 08:32:40 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 03 Oct 2023 08:32:40 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:32:45 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 03 Oct 2023 08:32:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Oct 2023 08:32:45 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 03 Oct 2023 08:33:02 GMT
RUN boot
# Tue, 03 Oct 2023 08:33:02 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 03 Oct 2023 08:33:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Oct 2023 08:33:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0f8e5bf90a9369ab6f51e945ac866f2ec10afab1f1331f92ddd272ac850a21`  
		Last Modified: Tue, 03 Oct 2023 08:41:12 GMT  
		Size: 143.5 MB (143543520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0f6a7f07764db108be0aaa82c5a25b133b9b05a3288e6f3c74f4d6bdb28f74`  
		Last Modified: Tue, 03 Oct 2023 08:41:02 GMT  
		Size: 1.1 MB (1064815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e88b16f2a183af927cb1bf26c97523b0b5ff6e5ca627920f854703ed89a276`  
		Last Modified: Tue, 03 Oct 2023 08:41:06 GMT  
		Size: 58.8 MB (58820386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d350b6811ebdcd330097f0005fe9d86655bbff17eba68845816805771404a967`  
		Last Modified: Tue, 03 Oct 2023 08:41:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
