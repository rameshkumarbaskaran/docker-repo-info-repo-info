## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:85e0eb4efdf7750e10ee2dbb4ff3bf8911e3d615cbd94bb854c96b9122056a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0f0c5d28f0032a5aa8409c4c0993ffe3ebea21f86bfd20ae8534fcdccb7b2816
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219832256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c7acba3ec11cee50c1ff44cfa9bd13bcf48a74f552e4a7db0f1c21b9c2969`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:59 GMT
ADD file:da3938f00f114fa8f5948fb7182da39c43e5ce57a334ba528681cb29aff0d2f6 in / 
# Wed, 01 Nov 2023 00:21:00 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:13:03 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:13:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:13:04 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:13:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:13:04 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:13:10 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:13:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:13:10 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:13:28 GMT
RUN boot
# Wed, 01 Nov 2023 01:13:28 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2f088d622efd8dbaa13d01eafd0aac8f9f33bb335edd3be897ae8059338c7bf7`  
		Last Modified: Wed, 01 Nov 2023 00:25:49 GMT  
		Size: 55.1 MB (55058052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4705af72d20463a1d7959017b897c1d186f4faa50f9cbea6f81f6c9fe7263182`  
		Last Modified: Wed, 01 Nov 2023 01:33:31 GMT  
		Size: 103.6 MB (103585016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2610742667f1b81154e783190c4ac660b1d3718ea17093a0d311ec87c4eb78f`  
		Last Modified: Wed, 01 Nov 2023 01:33:23 GMT  
		Size: 2.4 MB (2368719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0235d0a627bc4954514acdc106ca0016dbd80d1329acfd2c4cfa5bcec31a2e8`  
		Last Modified: Wed, 01 Nov 2023 01:33:27 GMT  
		Size: 58.8 MB (58820469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5bb3be96982f759da6dd05fd695c6b7d80013ab780ae2a9f6e528ea349480304
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217576631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b90ccd92272cd6c39e75c7fb27e9cf81a13d0b38ab11520371e0924816125f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:45:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 18:45:22 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 11 Oct 2023 18:45:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:45:24 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 11 Oct 2023 18:45:24 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 11 Oct 2023 18:45:25 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 18:45:30 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 11 Oct 2023 18:45:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 11 Oct 2023 18:45:30 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 11 Oct 2023 18:46:06 GMT
RUN boot
# Wed, 11 Oct 2023 18:46:06 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9023335902a8e4a34ef793a0035a716a10c893a34643861db03f1be029c9a229`  
		Last Modified: Wed, 11 Oct 2023 18:56:11 GMT  
		Size: 102.7 MB (102690464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a6c1e2627e751b53cb51ba0b7e179bf95c2c5cf9aa0a95d638a2d80d4a8f15`  
		Last Modified: Wed, 11 Oct 2023 18:56:04 GMT  
		Size: 2.4 MB (2357466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f69a4d20a4147d1e13e47eb42b57803a93e8daa869e3a1527529a2fb122b3e`  
		Last Modified: Wed, 11 Oct 2023 18:56:07 GMT  
		Size: 58.8 MB (58820891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
