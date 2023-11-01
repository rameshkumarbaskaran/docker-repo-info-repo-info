## `clojure:temurin-17-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:e4d71a05bc1e585a27bfd6c9380872a6801e3fb204daa61b33b38a5f868bf07a
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
$ docker pull clojure@sha256:87bfd5be44c74b6fc0d24ff87b69d154d9e3a3d831e101c48a4880b9ecced71d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235006663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49cbb43149ca509c0b6f80a890b08ca39acfd4ae1f77e6ed3d3a9d01b5448de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:05:28 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 01:05:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 01:05:31 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 01:05:32 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 01:05:32 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 01:05:37 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 01:05:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 01:05:37 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 01:05:54 GMT
RUN boot
# Tue, 31 Oct 2023 01:05:54 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 31 Oct 2023 01:05:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 31 Oct 2023 01:05:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed13091dc8653df4bb00fe6e6584527ee55d9420cf9bf1d72fd4e280fb96c81a`  
		Last Modified: Tue, 31 Oct 2023 01:22:39 GMT  
		Size: 143.7 MB (143681739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35accde96f2828bb96fecdc7ecb136bc3f45bbf3ff939d186a38cdbe60b5fb6b`  
		Last Modified: Tue, 31 Oct 2023 01:22:30 GMT  
		Size: 3.3 MB (3324883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd790d3e63b7ae8cd44a1a71e47845501ef6a4c6e3cb8e1269193d9ee40c570`  
		Last Modified: Tue, 31 Oct 2023 01:22:33 GMT  
		Size: 58.8 MB (58820358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919548864db59df75fefb78af1cd480998dde196f60294b62d05fa19ec5c57f9`  
		Last Modified: Tue, 31 Oct 2023 01:22:29 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
