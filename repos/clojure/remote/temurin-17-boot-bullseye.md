## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:2bc9cb94c05e3bcbfa5ea7b3c174e944e717634cd909749e4606290ec5b7324f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:00ba9d8c6796147225639e3895e93267b90fe39fe90f37a3fea459a96bb3d6b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261121282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262c9f44b218ccba1e789be1ed29cd624bbbf48653d8d0073600d100b0d36dc6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:59 GMT
ADD file:da3938f00f114fa8f5948fb7182da39c43e5ce57a334ba528681cb29aff0d2f6 in / 
# Wed, 01 Nov 2023 00:21:00 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:23:38 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:23:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:40 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:23:40 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:23:40 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:23:45 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:23:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:23:46 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:24:02 GMT
RUN boot
# Wed, 01 Nov 2023 01:24:02 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Nov 2023 01:24:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Nov 2023 01:24:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2f088d622efd8dbaa13d01eafd0aac8f9f33bb335edd3be897ae8059338c7bf7`  
		Last Modified: Wed, 01 Nov 2023 00:25:49 GMT  
		Size: 55.1 MB (55058052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcddd2ced9b19df156d3ed20c740fcd9fb5a05a9908fc224ced26758a55c9b92`  
		Last Modified: Wed, 01 Nov 2023 01:40:29 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f9f584d9660ec36cc74210df9bb11021a388f09c4d0e0a5c6b377646ce7940`  
		Last Modified: Wed, 01 Nov 2023 01:40:18 GMT  
		Size: 2.4 MB (2368712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc32f40d04486497aa612684fc1b5fdc1e62803b42a0e027a7f12678dd1e28a`  
		Last Modified: Wed, 01 Nov 2023 01:40:21 GMT  
		Size: 58.8 MB (58820216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43547bdaa9370f0858b3be8af2daafd672ca7007126d03ad6d397ca12e9c60e`  
		Last Modified: Wed, 01 Nov 2023 01:40:17 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9f623dc8397658200c44308550ceffec34ce378a2600d6ff374744d8554d7db2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258567934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc76eef32003845f4fa0aa9060a870354d5eb8a7dcb3180436c95fb40e0254f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:45:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:01 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 01:06:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 01:06:05 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 01:06:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 01:06:05 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 01:06:10 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 01:06:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 01:06:10 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 01:06:30 GMT
RUN boot
# Tue, 31 Oct 2023 01:06:31 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 31 Oct 2023 01:06:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 31 Oct 2023 01:06:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90039ec2f4fe2b5cdd7b80a6438242b4a123b1c3880a1f5babfa9b9b475835ae`  
		Last Modified: Tue, 31 Oct 2023 01:22:59 GMT  
		Size: 143.7 MB (143681710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7566ab1e852d59d8d1ab59156cd3e655c40542d25b9158b35db5b336046f46a0`  
		Last Modified: Tue, 31 Oct 2023 01:22:48 GMT  
		Size: 2.4 MB (2357465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8b1868cd16dd5662a7fb76ffda86a3824629dc7e8713c4abc80206a5b02033`  
		Last Modified: Tue, 31 Oct 2023 01:22:51 GMT  
		Size: 58.8 MB (58820548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d60807bcd8345a598d36514e6bea7c39fd8a0baa2d5696d30bdb8596b533b6`  
		Last Modified: Tue, 31 Oct 2023 01:22:48 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
