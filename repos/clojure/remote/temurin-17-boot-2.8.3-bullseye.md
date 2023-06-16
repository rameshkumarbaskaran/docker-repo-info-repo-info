## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:75d6ad183cd5dc5919301f55bfb9ad85af83e687bda5b93e6e365c576294059e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5bffa05b86e202d199ac97b408f90cee6bb8d9775631230d8875a38fe1910c82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308818463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4cbc99a1ee22a90ba482c2ddd7efe82b500228e81f4d012df6f4875368768f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:54 GMT
ADD file:e530b0563ea53d97b2f28e62149a665900196f86611df99a88c7a8ab2097b95d in / 
# Mon, 12 Jun 2023 23:20:54 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 06:32:20 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Fri, 16 Jun 2023 06:32:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 06:32:22 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Jun 2023 06:32:22 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Jun 2023 06:32:22 GMT
WORKDIR /tmp
# Fri, 16 Jun 2023 06:32:28 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Jun 2023 06:32:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jun 2023 06:32:28 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Jun 2023 06:32:47 GMT
RUN boot
# Fri, 16 Jun 2023 06:32:47 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 16 Jun 2023 06:32:47 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jun 2023 06:32:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:93c2d578e4211e82e47e7ada9ed05d1869a2362c6f7509f2ee8d91ccebfb7fbd`  
		Last Modified: Mon, 12 Jun 2023 23:26:08 GMT  
		Size: 55.1 MB (55055162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4515753016cb9505ce2733cb1ed2889c8ac635d7a4b54493c197cb07f13021`  
		Last Modified: Fri, 16 Jun 2023 06:43:19 GMT  
		Size: 192.6 MB (192580329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b223b82fe118f7ac0390aec38c67e3a6dd79da9863b5a16f67bfbce2e553f1b`  
		Last Modified: Fri, 16 Jun 2023 06:43:05 GMT  
		Size: 2.4 MB (2362089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919a46dbfee87ef9017db2665f5e4818261e87b2e92b1025e52b9ff7b19fb931`  
		Last Modified: Fri, 16 Jun 2023 06:43:09 GMT  
		Size: 58.8 MB (58820482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e600408bc6743dbfcd26b916bdf2183c563797fa46c01ca4eb0852c8170c56`  
		Last Modified: Fri, 16 Jun 2023 06:43:05 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6411c8fa1af47017998a971e46d5d74cc4af554e980329da73d84adbbea29cc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.3 MB (306263931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d42ee4c7dc2fe1b83e1ea78ac48188103d64aa809c7a5afe3cd8edb0eeb3431`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:22 GMT
ADD file:caddd2f40296ec5c1bf7487617ca8694cfff9a1d9b7484159e203b6514cb5f5f in / 
# Mon, 12 Jun 2023 23:40:23 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:50:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 04:46:29 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Fri, 16 Jun 2023 04:46:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:46:33 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Jun 2023 04:46:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Jun 2023 04:46:33 GMT
WORKDIR /tmp
# Fri, 16 Jun 2023 04:46:38 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Jun 2023 04:46:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jun 2023 04:46:38 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Jun 2023 04:46:56 GMT
RUN boot
# Fri, 16 Jun 2023 04:46:56 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 16 Jun 2023 04:46:56 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jun 2023 04:46:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:663ccfaf62a5d7b997bca03d1dc6d5dfff01b9e0de08d86dbea8957ea92d7d16`  
		Last Modified: Mon, 12 Jun 2023 23:44:25 GMT  
		Size: 53.7 MB (53704136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172252176b2d2b44f66626001ffedf36355c238558bbc403980303e6b6c92ae9`  
		Last Modified: Fri, 16 Jun 2023 04:56:58 GMT  
		Size: 191.4 MB (191387640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d209f9a9a585297e98927ab8aece778729273ea765bf993bb6486bf27fb93c`  
		Last Modified: Fri, 16 Jun 2023 04:56:47 GMT  
		Size: 2.4 MB (2351326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7b155d8f7d2e9e0af3797d52f2d75d2183be3414ac33775d731a870d7199d0`  
		Last Modified: Fri, 16 Jun 2023 04:56:50 GMT  
		Size: 58.8 MB (58820431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29a311b04bd6c06a341b1cb4a27fae423071a6c36312dead7470b3f4208df1d`  
		Last Modified: Fri, 16 Jun 2023 04:56:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
