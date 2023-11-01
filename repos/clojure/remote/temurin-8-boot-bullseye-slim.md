## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:3a75804616411691cdd8860fea9e72ba96ddc9e6934fc8026d21f808ad0df751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4e4db6bd8c1f81b7096fb5887053192fbaa12a0798cecb6c7bc3732321de5a76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194902843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13df102d93ec85e839551ca44a090e6f817aae5f246c687aefceb91c5b158a6e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:13:32 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:13:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:13:33 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:13:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:13:33 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:13:38 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:13:38 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:13:57 GMT
RUN boot
# Wed, 01 Nov 2023 01:13:57 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c66b33f7eb79686c34c20de69338a756f72b6eaba81919c78ee81be81cdcd2`  
		Last Modified: Wed, 01 Nov 2023 01:33:48 GMT  
		Size: 103.6 MB (103585016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b4a20306e6df82bad64c0aa35f6755dee5df63c41b8bc5deffc22da99b9138`  
		Last Modified: Wed, 01 Nov 2023 01:33:40 GMT  
		Size: 1.1 MB (1079439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ec193bdab1c4996de7d62a069abfc280329d32884e3a265aa1cd807b49c98a`  
		Last Modified: Wed, 01 Nov 2023 01:33:43 GMT  
		Size: 58.8 MB (58820473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:28f97c608008ee863f07675a01649cc6693ff4ac552cc956e32a0482a16bbcfa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192641715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacc125bf7a98909ee68dadb6d5a7a9bc38863f2a7cc9ed26bb0e01b15481797`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:23:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 02:23:18 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 01 Nov 2023 02:23:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:23:21 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 02:23:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 02:23:21 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 02:23:26 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 02:23:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 02:23:26 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 02:23:43 GMT
RUN boot
# Wed, 01 Nov 2023 02:23:43 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35643da71287664512ea8bdb07a95ea4e9fd1ea39999012466c0333793c0ec82`  
		Last Modified: Wed, 01 Nov 2023 02:41:56 GMT  
		Size: 102.7 MB (102690497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab6c7854126e5d3e2d512ca6113dfda77978c31f1720ffddc63ab8d2a08e331`  
		Last Modified: Wed, 01 Nov 2023 02:41:48 GMT  
		Size: 1.1 MB (1066837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c22a2d0807dd0262e597732ee0751cf797ebf430826886ce56f5f7c42d844d`  
		Last Modified: Wed, 01 Nov 2023 02:41:51 GMT  
		Size: 58.8 MB (58820476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
