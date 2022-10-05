## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:b0423d3709150c9ccab5c277daa4b29dec1ee49abc54c13d51591bee9ce8be3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:43a61a5fbb043bf32af793481966fcaadea5490873ccebd4a487f5a3fb11ed33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194831854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e6bbb2ea660f01de4bbff029b5db4ea41f583ab4c2fb009e218b599415a2a4`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:31:08 GMT
COPY dir:300027169ac55d8fb6f67a0995ca298d5de23ab51f3dc8e227f6e221abd3d2c3 in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:31:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:31:09 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 01:31:09 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:31:09 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:31:15 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 01:31:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:31:15 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 01:31:40 GMT
RUN boot
# Wed, 05 Oct 2022 01:31:41 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d3b033801fe47b9b71e1e237e407fb11abe76a075f56d43fe9df4833ebe075`  
		Last Modified: Wed, 05 Oct 2022 01:46:08 GMT  
		Size: 103.5 MB (103513854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65942f418c7d3f0fa0b3ec1bf424b8c92f4f9fad47e1df08ce8f110f6fadee41`  
		Last Modified: Wed, 05 Oct 2022 01:45:59 GMT  
		Size: 1.1 MB (1077316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b460650406dd6aa6c6ec3c459c8a42267da8cb5dc686a25fdccdf774b597483a`  
		Last Modified: Wed, 05 Oct 2022 01:46:02 GMT  
		Size: 58.8 MB (58820582 bytes)  
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
