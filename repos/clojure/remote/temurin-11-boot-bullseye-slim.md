## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:aaedfd496007eb9a6982f3adb0fda128fe389b920fe9fad2d9a83c1d03e49302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ccfa42d07d3c57bbd0752c3cc1916a206648dff565fb35600dcbb1301f65ad1e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289442876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359f0713f859a07929ac974ecc8bd53b2e45e9d6d933dfb6b6568033ad6b2b88`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:34:29 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:34:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:34:31 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 01:34:31 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:34:31 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:34:37 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 01:34:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:34:37 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 01:35:00 GMT
RUN boot
# Wed, 05 Oct 2022 01:35:00 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd943cda847b9f3402014ae85cb3f413d8a8197a5743326a30702a399bd52788`  
		Last Modified: Wed, 05 Oct 2022 01:48:04 GMT  
		Size: 198.1 MB (198124862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15003a6d6fd77eef55e77fa2de024f1bfff0c4344db3ae24fcb30133651fbe70`  
		Last Modified: Wed, 05 Oct 2022 01:47:49 GMT  
		Size: 1.1 MB (1077308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69e16a07647248f4887a2d080e359d6bfc34f17d97f3aeebea3975bb7f380bf`  
		Last Modified: Wed, 05 Oct 2022 01:47:53 GMT  
		Size: 58.8 MB (58820604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:494aea102630b4bb1c354e436f1144d3b43306d7c51c7657158aca00668fc041
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284607225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269840f66ac8367dc9b3495c4a375da9514980e5f9e897dd952442e9211dea35`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 00:57:35 GMT
COPY dir:d8305eb424636b15e2ee68b77e921283e709f5d3d0768819ef40e6c325c7578e in /opt/java/openjdk 
# Wed, 05 Oct 2022 00:57:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 00:57:36 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 00:57:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 00:57:38 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 00:57:45 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 00:57:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 00:57:46 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 00:58:01 GMT
RUN boot
# Wed, 05 Oct 2022 00:58:01 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36823226c948e675df283a37335f66a71f8cd0ad8b4c380702959a9b3a6be822`  
		Last Modified: Wed, 05 Oct 2022 01:16:11 GMT  
		Size: 194.9 MB (194867812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98ef2bf09b0d60030aabf9de51fa188df2b80acb7517f9c1e54c7e897da236c`  
		Last Modified: Wed, 05 Oct 2022 01:15:54 GMT  
		Size: 859.3 KB (859260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736659ea8096e3ff4e962738e59424a42f865a2205199436ca3aad85e5f1e447`  
		Last Modified: Wed, 05 Oct 2022 01:15:58 GMT  
		Size: 58.8 MB (58815758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
