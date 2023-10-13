## `clojure:temurin-17-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:870882393aee283efe52c23ffbb287387d34bc518a145abc2affa804fcd076bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a7cc82829ce94db075a6855f558a7eeb2c9a42f77f0e4ab116ee634a83c5b1e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236247802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7219a8fed8ff3e36da6821a2b375bfc0d76b555b6feb7fe61d18c3c61ba33a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:52:38 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Fri, 13 Oct 2023 12:52:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 12:52:40 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 12:52:40 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 12:52:40 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 12:52:46 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 12:52:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 12:52:46 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 12:53:03 GMT
RUN boot
# Fri, 13 Oct 2023 12:53:03 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 12:53:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 12:53:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a34b75927f2306868c4a7fe1a7e58cbd84682bb3f607d3c9b61603d11b9ef3d`  
		Last Modified: Fri, 13 Oct 2023 13:10:13 GMT  
		Size: 144.8 MB (144775764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be64e0e8f8771d68c6401bde11e2fccd772a183919126ebcac00f0d96ea7898e`  
		Last Modified: Fri, 13 Oct 2023 13:10:02 GMT  
		Size: 3.5 MB (3501424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539afccd14051b85cc8571f66b364972e4ec5c6ddbeb85946e28b484fcbc33b4`  
		Last Modified: Fri, 13 Oct 2023 13:10:06 GMT  
		Size: 58.8 MB (58820341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b31d9dc789ff29a60dc394d7c9d8162b53fdbe8d11100e30a9b4d1145a39fce`  
		Last Modified: Fri, 13 Oct 2023 13:10:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:973e9587d176ce60bb96228f8eb6416c3dc4888ce6b9e698ffb29522b370d06d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234868783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d7eb9f9843d85cc9645c5786bee7a3b97ee79d3825d04e510ef7ea24f87bb8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 10:19:14 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Fri, 13 Oct 2023 10:19:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 10:19:16 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 10:19:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 10:19:16 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 10:19:21 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 10:19:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 10:19:22 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 10:19:38 GMT
RUN boot
# Fri, 13 Oct 2023 10:19:38 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 10:19:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 10:19:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff307ae0c323a4d6fd223fe9031e67bc368768a88263d2cc046c321b0bcaacfb`  
		Last Modified: Fri, 13 Oct 2023 10:34:23 GMT  
		Size: 143.5 MB (143543485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0129ab8a05b0f79fd763aa980479e1bf54a0bc9530ba74ee0f2e78450d1e62`  
		Last Modified: Fri, 13 Oct 2023 10:34:13 GMT  
		Size: 3.3 MB (3325227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b1129dbe57126596f0cbef86af0356bd34ca7ed678b6562e0d56383d3b6765`  
		Last Modified: Fri, 13 Oct 2023 10:34:17 GMT  
		Size: 58.8 MB (58820387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006ca18e9c5977aa937dc2ff02901cedbb08e7c308adb86a604d1b3718d92350`  
		Last Modified: Fri, 13 Oct 2023 10:34:13 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
