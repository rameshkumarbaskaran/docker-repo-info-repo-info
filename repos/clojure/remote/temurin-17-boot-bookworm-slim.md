## `clojure:temurin-17-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:54bf3cbb8c17c4df89aa5514971d2102a20290b0b695497fe69c45ad2243797c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:244f63c824eb8916b27a6265ea847ff6db43a57b271e61a1ea55360d4a60bafe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236346190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bda680e08e47694c70fa6e43a48b7bb2a30f31c7bad892ca1098d8b6a0e96a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:12:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:23:04 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:23:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:05 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:23:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:23:06 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:23:12 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:23:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:23:12 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:23:30 GMT
RUN boot
# Wed, 01 Nov 2023 01:23:30 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Nov 2023 01:23:30 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Nov 2023 01:23:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f66d533080f21b1abb7d6c1122fda3614b0c857f92230dfc024d06a8a930ab`  
		Last Modified: Wed, 01 Nov 2023 01:40:08 GMT  
		Size: 144.9 MB (144873950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bca7151c3e23c890b23a07ee852803cd3a0f2afebb178cb3d8311fb8225ba4`  
		Last Modified: Wed, 01 Nov 2023 01:39:58 GMT  
		Size: 3.5 MB (3501668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446a148b4f2571acaf9b5be91c127f2b3b96d642f6c6433bd019b0a400c9f83d`  
		Last Modified: Wed, 01 Nov 2023 01:40:01 GMT  
		Size: 58.8 MB (58820335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123a5fa0af7d3d45f06c770b140ae3b99f80a189c840bf744fd1ffdd5f7c954b`  
		Last Modified: Wed, 01 Nov 2023 01:39:57 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3cad4abf7cbec613841bc13395862121a54dae39a3b681c3c416ad73d7b818b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235006668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7821c794a08124816b74a42dffb6bdd876af0d404452891cb5ed11f8dbb41ae3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:22:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 02:31:59 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Wed, 01 Nov 2023 02:32:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:32:03 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 02:32:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 02:32:03 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 02:32:08 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 02:32:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 02:32:09 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 02:32:25 GMT
RUN boot
# Wed, 01 Nov 2023 02:32:26 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Nov 2023 02:32:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Nov 2023 02:32:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86f97d6646348cd45057676b9fafba41e447b62c4e4f82bfbc1b3dafa27b283`  
		Last Modified: Wed, 01 Nov 2023 02:47:50 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f01b9ae744d1fcaec9c08db6dea77bad882a7677b9b03025d5f42c051a9b5ba`  
		Last Modified: Wed, 01 Nov 2023 02:47:40 GMT  
		Size: 3.3 MB (3324911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7324f668820ef5d62d4a9d1c39fab97d0c140bfe929b0f6c59343f5b195772a4`  
		Last Modified: Wed, 01 Nov 2023 02:47:43 GMT  
		Size: 58.8 MB (58820526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a2fc84b3ba4641d699cd9ebae3ad8b780aebd34626cce5e3366851e8bc4113`  
		Last Modified: Wed, 01 Nov 2023 02:47:40 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
