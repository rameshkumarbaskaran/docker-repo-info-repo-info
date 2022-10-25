## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:c4ccbfd4f2900b0801e4f6d6ba5e7cf09e6c3acc10763be269900954043897ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:354714b226a24f34d22324fbe1a7f658518c11494eadddf48b499da85254aea8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194833586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa914590f5235e250b40da1964928c41218726316d7dfe15d39144f0357741d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Oct 2022 02:33:27 GMT
COPY dir:300027169ac55d8fb6f67a0995ca298d5de23ab51f3dc8e227f6e221abd3d2c3 in /opt/java/openjdk 
# Tue, 25 Oct 2022 02:33:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 02:33:28 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 25 Oct 2022 02:33:28 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 25 Oct 2022 02:33:28 GMT
WORKDIR /tmp
# Tue, 25 Oct 2022 02:33:34 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 25 Oct 2022 02:33:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 25 Oct 2022 02:33:34 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 25 Oct 2022 02:34:06 GMT
RUN boot
# Tue, 25 Oct 2022 02:34:06 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c8fc7384965746c1eff2e3c90a689ae0048d4ae23d30592f0dd0e23c474bc5`  
		Last Modified: Tue, 25 Oct 2022 02:48:26 GMT  
		Size: 103.5 MB (103513848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e761cc838647a81af74d26418b6fac8922ce80f68fb3745f8c821b74bca77835`  
		Last Modified: Tue, 25 Oct 2022 02:48:17 GMT  
		Size: 1.1 MB (1078981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039d22bc141dc11dbfe00f92a4c4f2cc06d29c76f194ea734585656856c378a1`  
		Last Modified: Tue, 25 Oct 2022 02:48:20 GMT  
		Size: 58.8 MB (58820719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b3cad1358f55f92b042256ec1079269bc431ab40d45e3618899efa6876a2a612
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192353372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3523ad956957d328bfe3810c33c3cb6966389724aa6f22cd3a55c0e367036c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 00:53:54 GMT
COPY dir:7668b70c49687fddef57006c57f288afd02ec3ccd6cde9cbc5231ec8fb9225f1 in /opt/java/openjdk 
# Wed, 05 Oct 2022 00:53:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 00:53:56 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 00:53:57 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 00:53:58 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 00:54:04 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 00:54:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 00:54:06 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 00:54:21 GMT
RUN boot
# Wed, 05 Oct 2022 00:54:22 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911611afa665b0683fbe96bda4abb9185fe2c620cdfcc9b8a6381b9fdee36056`  
		Last Modified: Wed, 05 Oct 2022 01:13:35 GMT  
		Size: 102.6 MB (102613711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e525ffd6380a2240e715a1cc90ce9121b1b4ab92837604b3ec3b8539913683`  
		Last Modified: Wed, 05 Oct 2022 01:13:24 GMT  
		Size: 859.3 KB (859269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c360ba1909394fb7e44f02c6e91a7494fb3e94d412574f9c90615882b13ce54c`  
		Last Modified: Wed, 05 Oct 2022 01:13:29 GMT  
		Size: 58.8 MB (58815997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
