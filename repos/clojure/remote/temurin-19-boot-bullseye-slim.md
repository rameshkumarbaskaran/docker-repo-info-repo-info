## `clojure:temurin-19-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:4d8465621ce08c2ffc8a8be7b8cef0f7c7c5c22f9bebed2f124c9a96a777d6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:897ae5abcaf0331497e02f70fffc6eb80e8ba2ee05ddc0ac51030b1b04c87abb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292423352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14de5744a5c3e0fe42c4025b6c5962a060d6a8ca6d147eb071e9240951f50d7a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Nov 2022 19:51:27 GMT
COPY dir:fef581854733ec7202f8c807463b9e1952aeb6c7a002719c7e54987e50ea4dcb in /opt/java/openjdk 
# Tue, 08 Nov 2022 19:51:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Nov 2022 19:51:29 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 08 Nov 2022 19:51:29 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 08 Nov 2022 19:51:29 GMT
WORKDIR /tmp
# Tue, 08 Nov 2022 19:51:35 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 08 Nov 2022 19:51:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 08 Nov 2022 19:51:35 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 08 Nov 2022 19:51:54 GMT
RUN boot
# Tue, 08 Nov 2022 19:51:55 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 08 Nov 2022 19:51:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 08 Nov 2022 19:51:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10a8a6939ae868ebbacdafba32bb072252658a353d99bfac452b469d292956a`  
		Last Modified: Tue, 08 Nov 2022 20:01:13 GMT  
		Size: 201.1 MB (201103390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d50d4b09c9b03c0185a3a4ee50c7fb5d2fac9aae43d1a33a8a33433a9d6789`  
		Last Modified: Tue, 08 Nov 2022 20:00:58 GMT  
		Size: 1.1 MB (1078995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb1940368efa86defb95e9fe4e828e61659cd7b40d4a70ccc0d7484b38acd3a`  
		Last Modified: Tue, 08 Nov 2022 20:01:01 GMT  
		Size: 58.8 MB (58820530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6b12b88280a01e6462e8e2b4e7b204027c51c2ea281926ed573ec2b81dd85d`  
		Last Modified: Tue, 08 Nov 2022 20:00:58 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f5c0e9b33669444cff9a2a7a63095189b64775ebf20fbd6f8a95c3bb40182910
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289533608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160e8f90e9df88afb02cf51e122717a0ce4be1c4b8a9f8c3b21dbfaca48c732f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 15:49:24 GMT
COPY dir:2fc3a52010e404362374a6fbc2449d1ef85a3bc7bb00efe969cabc1864797789 in /opt/java/openjdk 
# Wed, 26 Oct 2022 15:49:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 15:49:29 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Oct 2022 15:49:29 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Oct 2022 15:49:29 GMT
WORKDIR /tmp
# Wed, 26 Oct 2022 15:49:34 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Oct 2022 15:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Oct 2022 15:49:34 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Oct 2022 15:49:51 GMT
RUN boot
# Wed, 26 Oct 2022 15:49:51 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 26 Oct 2022 15:49:51 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Oct 2022 15:49:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0786999deff23ea2618e481d077c8e627d22cb087604cb4be63e8e3940eac2be`  
		Last Modified: Wed, 26 Oct 2022 16:05:46 GMT  
		Size: 199.6 MB (199582448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ffb41de36a9d87eb76e623c99d27f9234dad396c2bc990fa3537b6d100f4e40`  
		Last Modified: Wed, 26 Oct 2022 16:05:34 GMT  
		Size: 1.1 MB (1066357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82d4f28e51b655654c865c54adc61f49cfe346f7ef37b8a237b344459bb6777`  
		Last Modified: Wed, 26 Oct 2022 16:05:37 GMT  
		Size: 58.8 MB (58820492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3420c49a0fcef9a7ba416353d8e143515143d63ff7db6b7a5a80290547e5b15d`  
		Last Modified: Wed, 26 Oct 2022 16:05:33 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
