## `clojure:temurin-17-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:be70e684842d2161ee2a1c8b4b710d6d28834f9196bf0ee1b3ec23f7938acb30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bb8b8cab8732b39aafde5929cf770f24777bf75973f1a9dba54dd32c1e240f1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236247729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7597662d245c9e92c15ff4cbeeeb6570e1db79c7a7609965b03236a3f812437`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:34:34 GMT
COPY dir:762e280751e9eaacf2bfae42d6a8cb2a49846426bd7c5675b21a4c0c8ae8fb71 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:34:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:34:35 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 01:34:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:34:35 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:34:41 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 01:34:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:34:41 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 01:34:59 GMT
RUN boot
# Fri, 13 Oct 2023 01:34:59 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:34:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:34:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb33a0642e97b629944310a73d2b5516fe91caf4addd502df39d147e81101246`  
		Last Modified: Fri, 13 Oct 2023 01:48:38 GMT  
		Size: 144.8 MB (144775771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3ec1a4a3bded2454deb0f005874736ebe6121fee5f9719a520fe9b629dc6dc`  
		Last Modified: Fri, 13 Oct 2023 01:48:27 GMT  
		Size: 3.5 MB (3501473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc0467d57e1a4aa98661dc3e6f1cd38a1238eb2e898d42614b0b1905655951e`  
		Last Modified: Fri, 13 Oct 2023 01:48:30 GMT  
		Size: 58.8 MB (58820211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0381ef3cd7063a1f485813653958d0bcd80d1113c274222f157eda348d7b10af`  
		Last Modified: Fri, 13 Oct 2023 01:48:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0e927b42ee0b2aee6abcb77693bd1d218bbabadc932980285feb86efbe150e0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234869027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0b5c10b401c1f8594ac956bc019d9c1ef0f1bda378996f4f18c6e966c87d40`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:05:21 GMT
COPY dir:9add47918f86acac35c907520d4811042633ac78a65fb2fbf0acc7586100f57a in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:05:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:05:24 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 01:05:25 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:05:25 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:05:30 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 01:05:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:05:30 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 01:05:48 GMT
RUN boot
# Fri, 13 Oct 2023 01:05:48 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:05:48 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:05:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4166017b3dfdb8fbf19b3063aec8aef41ca6e3d6c0e0f45f95bbf5bc223dddb2`  
		Last Modified: Fri, 13 Oct 2023 01:17:16 GMT  
		Size: 143.5 MB (143543519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6dcb9e4cf1ef2920e186f38b6124d85ef13188c7f7c7bc98ea3b7ccf72cefd`  
		Last Modified: Fri, 13 Oct 2023 01:17:07 GMT  
		Size: 3.3 MB (3325261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c5cf8881df6cabfd83640ba79d8a5c3a38f96e1a9e3e47ec498e55c90bfbdb`  
		Last Modified: Fri, 13 Oct 2023 01:17:10 GMT  
		Size: 58.8 MB (58820564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170aabb1488994911db90896eea02dacf5f7fb321b268080a9978b8cb34d1b8f`  
		Last Modified: Fri, 13 Oct 2023 01:17:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
