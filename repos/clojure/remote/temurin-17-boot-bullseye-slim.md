## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:d7f40a84d3fb064a884f3a365f318efbcc866fb4a9d4b8bcd74675dd8de1f1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:33d5b3cc93d20c9623b8096ec8c339f264e6d9f68a2f1c8dd616a8f0c70d126b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236093897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2c5b0148445f3954debf7ddd46d7beb329e8647290c18d83453eac87658238`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Fri, 13 Oct 2023 12:53:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 12:53:48 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 12:53:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 12:53:49 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 12:53:54 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 12:53:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 12:53:54 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 12:54:11 GMT
RUN boot
# Fri, 13 Oct 2023 12:54:11 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 12:54:12 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 12:54:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ed08f527e1354de75b3134c8eaf98a20167fca29b41180e318957ba857ca0b`  
		Last Modified: Fri, 13 Oct 2023 13:10:54 GMT  
		Size: 1.1 MB (1079486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542f22d705642a61446296cccbd35e695e8005d56c5c2b95b73b34235f2b1572`  
		Last Modified: Fri, 13 Oct 2023 13:10:57 GMT  
		Size: 58.8 MB (58820440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15427ef2d7582417fd19aa0d90d68bd6fc62e043d611b559b0da3be757316a2a`  
		Last Modified: Fri, 13 Oct 2023 13:10:53 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9d138d746dd01670a7286d3ffc6568ba16ec2f214755fb331e3bd44e597620d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233495102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b3e21e647dd6203a0288ff4419e8247af264d633c482f0071c07249d69bf28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Fri, 13 Oct 2023 10:20:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 10:20:08 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 10:20:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 10:20:08 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 10:20:13 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 10:20:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 10:20:13 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 10:20:30 GMT
RUN boot
# Fri, 13 Oct 2023 10:20:30 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 10:20:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 10:20:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba29605be7387d32f13d0a75a63f10f2144c1ced7c7e502d0cd66a45a5cf34ba`  
		Last Modified: Fri, 13 Oct 2023 10:34:50 GMT  
		Size: 1.1 MB (1066843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741620ee9613407d907cabd18abc6eacdb7330fa0cc47499452163eb05ad4dff`  
		Last Modified: Fri, 13 Oct 2023 10:34:54 GMT  
		Size: 58.8 MB (58820253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59c0e0da2f13e593d87148839c614eb6a3a520118b5436c13483d11a0ea6915`  
		Last Modified: Fri, 13 Oct 2023 10:34:49 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
