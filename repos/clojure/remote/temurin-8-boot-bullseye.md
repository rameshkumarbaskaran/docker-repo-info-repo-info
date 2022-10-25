## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:c97c256312f0696d161417ff39e4146904f6ec4a8591d15d6f95b80f49e2e700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c55b5178270382eb8cb4a7d647f3a6a239d03af8c848aa40a608ec0b051651a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219743300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383d0472c1cd26695f0016f150cbbff9c4d1c69a02d599deaa703fc43d48ad6b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Oct 2022 02:32:30 GMT
COPY dir:300027169ac55d8fb6f67a0995ca298d5de23ab51f3dc8e227f6e221abd3d2c3 in /opt/java/openjdk 
# Tue, 25 Oct 2022 02:32:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 02:32:31 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 25 Oct 2022 02:32:31 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 25 Oct 2022 02:32:31 GMT
WORKDIR /tmp
# Tue, 25 Oct 2022 02:32:37 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 25 Oct 2022 02:32:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 25 Oct 2022 02:32:38 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 25 Oct 2022 02:33:19 GMT
RUN boot
# Tue, 25 Oct 2022 02:33:19 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479a9f308d68e7fc10c050f0178ed5da63c43501be70a5e1990e6f5737383502`  
		Last Modified: Tue, 25 Oct 2022 02:48:07 GMT  
		Size: 103.5 MB (103513858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb1a818d1b8727005ebc4e34a7bb26b4c8141d910d5f357fcd82b8b0ee5e455`  
		Last Modified: Tue, 25 Oct 2022 02:47:58 GMT  
		Size: 2.4 MB (2362140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddaf57563cb23a0c8f730bbeacffeca8dd4c71bd22ffc5193d9b6eaa1ca50ba`  
		Last Modified: Tue, 25 Oct 2022 02:48:06 GMT  
		Size: 58.8 MB (58820970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c1df29ec7f00a248b1764b6cb3c2daab1f15edc2b8fb7cdd8e3859a6c734fc68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217274759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea69e79fc1d555f79f658a50732cf1275c0435615c0fd5a0f8bd62f6fc1a7a3`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 00:53:17 GMT
COPY dir:7668b70c49687fddef57006c57f288afd02ec3ccd6cde9cbc5231ec8fb9225f1 in /opt/java/openjdk 
# Wed, 05 Oct 2022 00:53:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 00:53:18 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 00:53:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 00:53:20 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 00:53:27 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 00:53:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 00:53:28 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 00:53:44 GMT
RUN boot
# Wed, 05 Oct 2022 00:53:44 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199e042cfdd7628b0f0e41afb373d86d7e0fb6385396b5a6fc0bec0d3533c7d6`  
		Last Modified: Wed, 05 Oct 2022 01:13:13 GMT  
		Size: 102.6 MB (102613748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562a763a8bd674c9c96cbba87fa131181612ea6b7e120ebd7b77828c2c721e31`  
		Last Modified: Wed, 05 Oct 2022 01:13:03 GMT  
		Size: 2.1 MB (2144447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816f1c39b89b9818b1056834fe57050a66da259da19eafd900c3b55f1dfc6c05`  
		Last Modified: Wed, 05 Oct 2022 01:13:08 GMT  
		Size: 58.8 MB (58815939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
