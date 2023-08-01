## `clojure:temurin-8-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:4f64540fba598bf75a5038c2b71b3a9aacdee4aa9f36785efa4351c11b6d2c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b8c8f1ef7db0e16487222853345ea027e9eb544f0e4a505ce0fb058ee6db11d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194900543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e784131f616a69391dfa47969a0a9d93d2c58614fe9b6d7ad6806b76eb1e6d3`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 01 Aug 2023 22:05:00 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Tue, 01 Aug 2023 22:05:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:05:01 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 01 Aug 2023 22:05:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 01 Aug 2023 22:05:01 GMT
WORKDIR /tmp
# Tue, 01 Aug 2023 22:05:07 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 01 Aug 2023 22:05:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 01 Aug 2023 22:05:07 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 01 Aug 2023 22:05:26 GMT
RUN boot
# Tue, 01 Aug 2023 22:05:26 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567fa53d58445e9c2f0ed4e6f4625dceeac843a03cecf021904aa8458a56dbcc`  
		Last Modified: Tue, 01 Aug 2023 22:15:34 GMT  
		Size: 103.6 MB (103585037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ccdfa0f01c891bf593cd5ccae70edb71360b3abdaa92e342c18422bc5bb51f`  
		Last Modified: Tue, 01 Aug 2023 22:15:25 GMT  
		Size: 1.1 MB (1077546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e1fe47dc20f20d49c896694ba7368dfae86201f6f57761cb289211c0180803`  
		Last Modified: Tue, 01 Aug 2023 22:15:28 GMT  
		Size: 58.8 MB (58820358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ccd124d8f8e73848f13a61911c978ca9bb41c3b18602255fc115300728e4178c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192638694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eefbe6861084c44812539d0885e06198bf6b898ebc2d1c807d8e16202700eea`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:25:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 01 Aug 2023 22:11:02 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Tue, 01 Aug 2023 22:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:11:04 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 01 Aug 2023 22:11:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 01 Aug 2023 22:11:04 GMT
WORKDIR /tmp
# Tue, 01 Aug 2023 22:11:09 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 01 Aug 2023 22:11:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 01 Aug 2023 22:11:09 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 01 Aug 2023 22:11:27 GMT
RUN boot
# Tue, 01 Aug 2023 22:11:27 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeec71f6c091e1e46dc0373eb0d5b1f4661ddef9abd0393e4f9896f82a717d1`  
		Last Modified: Tue, 01 Aug 2023 22:18:26 GMT  
		Size: 102.7 MB (102690458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18e53916da191690f61d55bd4146f55deae03ff27257519d255a05f50e387dc`  
		Last Modified: Tue, 01 Aug 2023 22:18:19 GMT  
		Size: 1.1 MB (1064833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b552cf5cc7988342b85baff47a6867aee8cfbd5f0c32c21af0e71a816832778`  
		Last Modified: Tue, 01 Aug 2023 22:18:23 GMT  
		Size: 58.8 MB (58820572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
