## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:c8ec7c2e7ee6b5813faae36daa9f12fa08f17d975256261d5b5441f80550e5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e7b17d4815729c12e900e3c23f6945c316f01c6a5cec7b8f51cf5d3252d52454
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219741510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5aa7109b75c42b5eb9b59430a22321c588fff0846a147228a954f3fdaa6e7e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:30:21 GMT
COPY dir:300027169ac55d8fb6f67a0995ca298d5de23ab51f3dc8e227f6e221abd3d2c3 in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:30:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:30:22 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 01:30:22 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:30:22 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:30:28 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 01:30:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:30:28 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 01:30:58 GMT
RUN boot
# Wed, 05 Oct 2022 01:30:58 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff7f6c810173240005bf7ffb9ab85f81f48ebdf31fbd7f77dfae79e1c463c97`  
		Last Modified: Wed, 05 Oct 2022 01:45:49 GMT  
		Size: 103.5 MB (103513856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826f94d1ea07f1ff78cc3e3f898554b1a19fe86eb409291d876c1135fa7c8e53`  
		Last Modified: Wed, 05 Oct 2022 01:45:41 GMT  
		Size: 2.4 MB (2360654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c11bd8b8ba13ff0ad3598731879e4b26b301a802bf96251af88582d2f5eb26`  
		Last Modified: Wed, 05 Oct 2022 01:45:44 GMT  
		Size: 58.8 MB (58820752 bytes)  
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
