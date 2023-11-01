## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:8135e401961edbfd60d12b9a5c7bdd944960eb9d9f3c52bb04656ae0ebd4d836
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
$ docker pull clojure@sha256:caa24f89c85dd82c4d97f8383b9c459f5e4b80fdc7862357b969e4c78ae8dd1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192642031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a552a51d8dbdb185671fc247628ac0f542c01ae43d61fa544fe85511694022`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 18:46:09 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 11 Oct 2023 18:46:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:46:11 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 11 Oct 2023 18:46:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 11 Oct 2023 18:46:12 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 18:46:16 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 11 Oct 2023 18:46:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 11 Oct 2023 18:46:16 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 11 Oct 2023 18:46:34 GMT
RUN boot
# Wed, 11 Oct 2023 18:46:34 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865ba808396777a6b8ccd88f4ace2c7e93ce0815719cc60a7da9ffb2bdb63662`  
		Last Modified: Wed, 11 Oct 2023 18:56:27 GMT  
		Size: 102.7 MB (102690512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63de560d7e7ee0a91861d7ef41397222bf1c7ad7e17b3680e4fde824d86a02a`  
		Last Modified: Wed, 11 Oct 2023 18:56:20 GMT  
		Size: 1.1 MB (1066851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1288a05683bd8f948d2f3f6729fc61655ec8a1d4beb85b9f762c46bcb95ce73`  
		Last Modified: Wed, 11 Oct 2023 18:56:25 GMT  
		Size: 58.8 MB (58820582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
