## `clojure:temurin-19-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:0d8f11e4457ae1edad31e43fc1f8ec6ebe5e4d8842c5879a6bbfcb1a4f0124fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e076a8224e82730849df1c184ef78248ae558a35aadf8ad910d372bff620796e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292162035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec33686e404014bba33323c0f42c862cd63ea385ba9ca268354193d5aed669e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:40:49 GMT
COPY dir:49a4548ab030e4d26793e92b4d74537cf530961ce7b4083b8d383585c96415d5 in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:40:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:40:51 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 01:40:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:40:51 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:40:57 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 01:40:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:40:57 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 01:41:17 GMT
RUN boot
# Wed, 05 Oct 2022 01:41:17 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:41:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:41:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e7de30eb4e390cffd51e73ffc9a011f0684ec59cf871eeee7182269b9d6507`  
		Last Modified: Wed, 05 Oct 2022 01:52:11 GMT  
		Size: 200.8 MB (200843776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d391723b27c3675727ffe4dfeae8370451553c0cdbbfa01ffd1315c1e0c9aff`  
		Last Modified: Wed, 05 Oct 2022 01:51:56 GMT  
		Size: 1.1 MB (1077338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93797ebaaa10c3a206a8467ae610910a0bdc79fdf60be42fa9dd309eac422632`  
		Last Modified: Wed, 05 Oct 2022 01:51:59 GMT  
		Size: 58.8 MB (58820420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2786c0615c1aef29a30d211544daeedf0b9c7aa9470a91847455244c7382c4bd`  
		Last Modified: Wed, 05 Oct 2022 01:51:55 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

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
