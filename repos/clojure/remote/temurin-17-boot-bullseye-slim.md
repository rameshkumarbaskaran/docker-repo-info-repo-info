## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:cde43030e5486349e772443266a313c44b2ada5d85cdf094cb439b3c3855fc21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7617531e6bc4b359af4e7b4946b574e1b43537fdb8052830d3957c5c40f04f54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 MB (283457348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc65a3b3594536ba7cf9fe8fd2724c1296e7abca681072f17e91ca833bad0e7c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 21:55:22 GMT
COPY dir:b50a87fd6710a805ef25d6c1dd2c5f7aa37ef63d04ab1c00c91801848dae94f0 in /opt/java/openjdk 
# Wed, 26 Oct 2022 21:55:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 21:55:24 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Oct 2022 21:55:24 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Oct 2022 21:55:24 GMT
WORKDIR /tmp
# Wed, 26 Oct 2022 21:55:30 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Oct 2022 21:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Oct 2022 21:55:30 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Oct 2022 21:55:49 GMT
RUN boot
# Wed, 26 Oct 2022 21:55:49 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 26 Oct 2022 21:55:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Oct 2022 21:55:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e670a3c00fcddd4db26555e9c844d563ed2f95a3a416c451f078b9d2826bd660`  
		Last Modified: Wed, 26 Oct 2022 22:11:01 GMT  
		Size: 192.1 MB (192137485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04e103a273182a3129f333fb8a2d0e9dc6164f280b10300f33aa240fc6f11c9`  
		Last Modified: Wed, 26 Oct 2022 22:10:46 GMT  
		Size: 1.1 MB (1078960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7757958abeb7b67d35a59a8bd45b9e62be19439dcee6809e22f8c0ddd59b99`  
		Last Modified: Wed, 26 Oct 2022 22:10:49 GMT  
		Size: 58.8 MB (58820467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073053101f9cc2fbeb0a8395e0052529f7f923cc4d5193042c1e5b9d9110d4d`  
		Last Modified: Wed, 26 Oct 2022 22:10:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:21a3be2b144bf61f7585c88cd0c8d71da0c4bf6ae08a51dda40872a4df30b01a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 MB (280855152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fbc73234a0d5c015b45cacf23d9bab218a8957944c3c90d71476902dfbcbfd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 15:45:22 GMT
COPY dir:580c509aa131da1d31de9db8eed968c1f0ef93ad270f258b0b43d9d7d72bba84 in /opt/java/openjdk 
# Wed, 26 Oct 2022 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 15:45:27 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Oct 2022 15:45:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Oct 2022 15:45:27 GMT
WORKDIR /tmp
# Wed, 26 Oct 2022 15:45:31 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Oct 2022 15:45:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Oct 2022 15:45:32 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Oct 2022 15:45:48 GMT
RUN boot
# Wed, 26 Oct 2022 15:45:49 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 26 Oct 2022 15:45:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Oct 2022 15:45:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5227b5452ba825facdc158312391c195512969f1ab7a485e56b2a432c2fcf433`  
		Last Modified: Wed, 26 Oct 2022 16:01:26 GMT  
		Size: 190.9 MB (190904076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afeb01f03f79cba2182a0ba0171a49e74856f06fa748f6189f985cbf6320d0d`  
		Last Modified: Wed, 26 Oct 2022 16:01:13 GMT  
		Size: 1.1 MB (1066327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf5db60693257df14b8da660eaec26b7ce78671057bcff86a0f792c663f860f`  
		Last Modified: Wed, 26 Oct 2022 16:01:16 GMT  
		Size: 58.8 MB (58820440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4281ef008ca27e429064da5a5c36da1729ddd7923577022525c612175fcbc8e`  
		Last Modified: Wed, 26 Oct 2022 16:01:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
