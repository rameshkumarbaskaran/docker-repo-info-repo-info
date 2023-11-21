## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:d7b3a695f381902adec9d4c61c413a1d24ebf65c7205f61b50c1fe60a393b35f
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
$ docker pull clojure@sha256:c576d07abbbb8c886ea04796aef7d230eda8a2b70e3910e2e8d87c087250890c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258567929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df20294d35487d7107b78f2dc03aa9da7031ce62232d25854a78f271d12e520`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:31:54 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:31:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 07:31:58 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 07:31:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 07:31:58 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 07:32:03 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 07:32:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 07:32:03 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 07:32:19 GMT
RUN boot
# Tue, 21 Nov 2023 07:32:19 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 21 Nov 2023 07:32:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Nov 2023 07:32:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d222093186fe627ebded7dede3ff589e904bd1961e248360a27dfa7ccf9ca30`  
		Last Modified: Tue, 21 Nov 2023 07:46:59 GMT  
		Size: 143.7 MB (143681718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa650dc54244f2e84da77a873cbbb3d8ee08d76ab6f6eefadc7e7821f3446a6a`  
		Last Modified: Tue, 21 Nov 2023 07:46:50 GMT  
		Size: 2.4 MB (2357488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a705bfb2d5221fadf9fa4d55a6f231924ee204dbd3769a043dc24fadba41c0`  
		Last Modified: Tue, 21 Nov 2023 07:46:53 GMT  
		Size: 58.8 MB (58820450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e49125a9198f3d3bc3d58796b6a7d347c272cae080f63d039ec4dd37ddd0be`  
		Last Modified: Tue, 21 Nov 2023 07:46:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
