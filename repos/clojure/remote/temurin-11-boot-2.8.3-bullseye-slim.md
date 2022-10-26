## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:5278448776c4ee8976abccf058a764b28b4d97e45bf24649d811b0895dcc12c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d28fd5f062a8455e3a4d49de4fb3f02db4d73de82eb8eb9671de298b2a2da85c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289444135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa97ab48bd408347802872571f1f4d8f4c417289166fc3ab0e3417a4a694d2bf`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 21:50:03 GMT
COPY dir:80db6f3290e8de5c875b6f069ca1d81f6b5c9f4e34668a64373c380a024a607d in /opt/java/openjdk 
# Wed, 26 Oct 2022 21:50:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 21:50:04 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Oct 2022 21:50:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Oct 2022 21:50:05 GMT
WORKDIR /tmp
# Wed, 26 Oct 2022 21:50:11 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Oct 2022 21:50:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Oct 2022 21:50:11 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Oct 2022 21:50:30 GMT
RUN boot
# Wed, 26 Oct 2022 21:50:30 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c841fe95a1d54b7ca4c2b99fafd39b67e5751811eec91ebb5a03381e515360e`  
		Last Modified: Wed, 26 Oct 2022 22:07:24 GMT  
		Size: 198.1 MB (198124716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bf1375d645308fc2e9b2e38a86f135357dab656f5eda19b3d3a2b19a5162ee`  
		Last Modified: Wed, 26 Oct 2022 22:07:10 GMT  
		Size: 1.1 MB (1078974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0fd864f507a1197cff42be2b5b617048154824c965553f636a0f6358f7f207`  
		Last Modified: Wed, 26 Oct 2022 22:07:13 GMT  
		Size: 58.8 MB (58820407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:156b1128238223d87e83562f5d807419f30e1b262b1e2aada48c6bbf26649d06
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284817691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee18e267e89b155b19e41efed3f3ac5faf3a1450f66a9e38263c94dcf0eccac`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 15:38:30 GMT
COPY dir:0c9c8c2b9cd43799d246d5824c591352650ad79f5d15544287f00c2deb1e4608 in /opt/java/openjdk 
# Wed, 26 Oct 2022 15:38:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 15:38:34 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Oct 2022 15:38:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Oct 2022 15:38:35 GMT
WORKDIR /tmp
# Wed, 26 Oct 2022 15:38:39 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Oct 2022 15:38:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Oct 2022 15:38:40 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Oct 2022 15:39:05 GMT
RUN boot
# Wed, 26 Oct 2022 15:39:05 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a3d7b35da3e357173d5404cc59df1a4394d6031ee4598b02de7918d2110bae`  
		Last Modified: Wed, 26 Oct 2022 15:58:03 GMT  
		Size: 194.9 MB (194866982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8efba58aed44cfe3eb1a9353e28bcc19d18fea23eb89deaee04bf4ad23b32d`  
		Last Modified: Wed, 26 Oct 2022 15:57:52 GMT  
		Size: 1.1 MB (1066323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f125baacd294c02c41c4afa3b7484f5f462c20f146ca4e02562d4b56f137da`  
		Last Modified: Wed, 26 Oct 2022 15:57:54 GMT  
		Size: 58.8 MB (58820476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
