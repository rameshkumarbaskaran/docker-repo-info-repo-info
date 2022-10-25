## `clojure:temurin-19-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:037169500ba4212d61504af596723ff9ffb01179e53a88d91a2040b45fcb970a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e3ca4cca7e8a53f5dfb205bb75151f24e38d7e2bc6e18c4d8bc0e927b273393c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292163678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f7feef748e078032bf633ac8216a44f5806279b05f32ee54f209c22f0d5d4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Oct 2022 02:43:04 GMT
COPY dir:49a4548ab030e4d26793e92b4d74537cf530961ce7b4083b8d383585c96415d5 in /opt/java/openjdk 
# Tue, 25 Oct 2022 02:43:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 02:43:05 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 25 Oct 2022 02:43:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 25 Oct 2022 02:43:06 GMT
WORKDIR /tmp
# Tue, 25 Oct 2022 02:43:12 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 25 Oct 2022 02:43:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 25 Oct 2022 02:43:12 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 25 Oct 2022 02:43:30 GMT
RUN boot
# Tue, 25 Oct 2022 02:43:30 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 25 Oct 2022 02:43:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 25 Oct 2022 02:43:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef26e3fe67290659a7b3a065746d54031cd623809f8df384628be68ee2d54a24`  
		Last Modified: Tue, 25 Oct 2022 02:54:40 GMT  
		Size: 200.8 MB (200843786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87eb45ac2b21603d6dbc013f3bc7ee8db0096db523ad3216748b9c7f3b1bb869`  
		Last Modified: Tue, 25 Oct 2022 02:54:25 GMT  
		Size: 1.1 MB (1078969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d80eae301b693cf079f018bbfd02028c30542acdc2baa47205eb744f99206cf`  
		Last Modified: Tue, 25 Oct 2022 02:54:29 GMT  
		Size: 58.8 MB (58820484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e60ac0629db00c6704cbe33c1894c1de24985934157a3aa7feb1b391e148155`  
		Last Modified: Tue, 25 Oct 2022 02:54:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:558b1bc00ca2905df3b45ba1ad8a56ae08fd4e5ace4e11f602c1aad24993fd5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289322703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71aa2face0a722193c8cf70ef91575c9ba4b904f0210b60c7d5ab46010ab37dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:05:12 GMT
COPY dir:58f6c37df253d3555e493197f96e3f21593e31d3faf1967e0a7b9d8f0ae9e30c in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:05:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:05:13 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 01:05:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:05:15 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:05:21 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 01:05:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:05:23 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 01:05:39 GMT
RUN boot
# Wed, 05 Oct 2022 01:05:40 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:05:40 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:05:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451966db02aec3760efec5b561c0d414315fc69df240034894ad8f6005b785c0`  
		Last Modified: Wed, 05 Oct 2022 01:21:02 GMT  
		Size: 199.6 MB (199582873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5982b44ce6838b4e0302d1721e64d76900e4546c98b60a6111ca551f4cd4865e`  
		Last Modified: Wed, 05 Oct 2022 01:20:45 GMT  
		Size: 859.3 KB (859285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c6a2bf63dd7e68b16bebda1d137a023680ee0139a973d15f195ad895d85a9b`  
		Last Modified: Wed, 05 Oct 2022 01:20:49 GMT  
		Size: 58.8 MB (58815751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aac136a81d8af5a18f5201d24ec4b105416801522789113cb5d5af6c7318c09`  
		Last Modified: Wed, 05 Oct 2022 01:20:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
