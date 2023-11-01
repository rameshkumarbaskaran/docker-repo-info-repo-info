## `clojure:temurin-8-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:177bbf97e2b0499ca263406759871474d99719280f2c40f6d3d4ec98c603265e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0f0c5d28f0032a5aa8409c4c0993ffe3ebea21f86bfd20ae8534fcdccb7b2816
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219832256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c7acba3ec11cee50c1ff44cfa9bd13bcf48a74f552e4a7db0f1c21b9c2969`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:59 GMT
ADD file:da3938f00f114fa8f5948fb7182da39c43e5ce57a334ba528681cb29aff0d2f6 in / 
# Wed, 01 Nov 2023 00:21:00 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:13:03 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:13:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:13:04 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:13:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:13:04 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:13:10 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:13:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:13:10 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:13:28 GMT
RUN boot
# Wed, 01 Nov 2023 01:13:28 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2f088d622efd8dbaa13d01eafd0aac8f9f33bb335edd3be897ae8059338c7bf7`  
		Last Modified: Wed, 01 Nov 2023 00:25:49 GMT  
		Size: 55.1 MB (55058052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4705af72d20463a1d7959017b897c1d186f4faa50f9cbea6f81f6c9fe7263182`  
		Last Modified: Wed, 01 Nov 2023 01:33:31 GMT  
		Size: 103.6 MB (103585016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2610742667f1b81154e783190c4ac660b1d3718ea17093a0d311ec87c4eb78f`  
		Last Modified: Wed, 01 Nov 2023 01:33:23 GMT  
		Size: 2.4 MB (2368719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0235d0a627bc4954514acdc106ca0016dbd80d1329acfd2c4cfa5bcec31a2e8`  
		Last Modified: Wed, 01 Nov 2023 01:33:27 GMT  
		Size: 58.8 MB (58820469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:abbe2104b2083267bb599a6456e9608a61e744ad38b807435943b5206349963f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217576070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a14b50c6b39bb5e6b6ef9333878638d5d77bc111eb162345ed4a6d8c6d1476`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:48 GMT
ADD file:f5677286e85ce6a345c7f5937e1ec576c37228e49c0fafe33574614c81cb7f76 in / 
# Wed, 01 Nov 2023 00:39:48 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:22:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 02:22:50 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 01 Nov 2023 02:22:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:22:53 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 02:22:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 02:22:53 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 02:22:58 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 02:22:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 02:22:58 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 02:23:15 GMT
RUN boot
# Wed, 01 Nov 2023 02:23:16 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d42ebdfc37acca5c3acbe173ac11133e691b402003a525c2b8431baf6935291e`  
		Last Modified: Wed, 01 Nov 2023 00:43:25 GMT  
		Size: 53.7 MB (53707757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1003c7122229a80b7dbbe3dace4e128ac86e5fd13e14a350774520e4719b064f`  
		Last Modified: Wed, 01 Nov 2023 02:41:39 GMT  
		Size: 102.7 MB (102690456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9fd82b41fd7d4810eb99b8a190cab978938742e310923c8061eb1d1f47853c`  
		Last Modified: Wed, 01 Nov 2023 02:41:32 GMT  
		Size: 2.4 MB (2357382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5beb14c49351672497fb61ee1fd2cefb288c45f475b6be3884a98d6b1e986c`  
		Last Modified: Wed, 01 Nov 2023 02:41:35 GMT  
		Size: 58.8 MB (58820475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
