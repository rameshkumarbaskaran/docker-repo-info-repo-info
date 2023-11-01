## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:e0392198bec787dce2312a01e5773a5f7e9008f99333a6633279fedceb6d29ee
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
$ docker pull clojure@sha256:83545e83aec7d7bd3bfeba3bf9bdd9fa4140e5f78e5f00d4af4c6e5125a2b6b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258567917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da249807bee061e503c7720466a246ebffd552e3ba16524d2014b24ab42db344`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:48 GMT
ADD file:f5677286e85ce6a345c7f5937e1ec576c37228e49c0fafe33574614c81cb7f76 in / 
# Wed, 01 Nov 2023 00:39:48 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:22:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 02:32:33 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Wed, 01 Nov 2023 02:32:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:32:36 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 02:32:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 02:32:37 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 02:32:41 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 02:32:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 02:32:42 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 02:32:59 GMT
RUN boot
# Wed, 01 Nov 2023 02:32:59 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Nov 2023 02:32:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Nov 2023 02:32:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d42ebdfc37acca5c3acbe173ac11133e691b402003a525c2b8431baf6935291e`  
		Last Modified: Wed, 01 Nov 2023 00:43:25 GMT  
		Size: 53.7 MB (53707757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f128160fac099412033f94426b8be1135c83b09e7bbf396c7c605d6aefd171b`  
		Last Modified: Wed, 01 Nov 2023 02:48:08 GMT  
		Size: 143.7 MB (143681747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c55c0e7a5f47eb05b2faf1267bf3cd0b81fb4b8837371b7821badc01733bb5`  
		Last Modified: Wed, 01 Nov 2023 02:47:59 GMT  
		Size: 2.4 MB (2357440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab8a2d685d3480a6519a6851fbd743140b2394d55c8cdb3147a957c0f19169a`  
		Last Modified: Wed, 01 Nov 2023 02:48:02 GMT  
		Size: 58.8 MB (58820575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02676bc49215091e142dceca7f6aec9dbab6514ed55858895c96b517cd07f36e`  
		Last Modified: Wed, 01 Nov 2023 02:47:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
