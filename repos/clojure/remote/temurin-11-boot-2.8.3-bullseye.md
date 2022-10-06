## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:3178a6edd8a4c43264317947de0ee5c72e742d038ca14a23882a2a721b73e6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9afdb38b79f944f5bca3879003bf24d5930cab7a86c5ead50eff93b167fc404f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314352493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee396b7c8de89a65bee1d92ac2e1e5cf1d39f1f3a5c2a75a8e202c9df43713f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:33:50 GMT
COPY dir:36d56a3b4865ff200a9bbbcc21ae60c89418e4eae9d60cbccb611641838bf98e in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:33:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:33:52 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Oct 2022 01:33:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Oct 2022 01:33:52 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:33:58 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Oct 2022 01:33:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Oct 2022 01:33:59 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Oct 2022 01:34:23 GMT
RUN boot
# Wed, 05 Oct 2022 01:34:23 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4ca2823c2d209cf0f2e558aa4af2216e66a915bea0f57552265e9d46d73fa6`  
		Last Modified: Wed, 05 Oct 2022 01:47:40 GMT  
		Size: 198.1 MB (198124887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e665f838905a407e09136eee0a80f95b68b6e3cbb2ccf737d83dd485a4fbba`  
		Last Modified: Wed, 05 Oct 2022 01:47:25 GMT  
		Size: 2.4 MB (2360748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387178cbe4c62530b8d96d4d2de501075a3f82c5b97bf9b0a5e49f8bc1da0e67`  
		Last Modified: Wed, 05 Oct 2022 01:47:29 GMT  
		Size: 58.8 MB (58820610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:281fcc7ea24ab860da9a0c1b91fa1b87f350b453a2ef8a490c35117c42ba2375
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309527506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af840642b192baf4379963b668706802d0c0330fa5348259440a2fa40e5a36a0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:31:52 GMT
COPY dir:0dc06d70d42a32ae203bdf41d3806f1204b90ca101c4efe4662ba862f2c76b8a in /opt/java/openjdk 
# Thu, 06 Oct 2022 02:31:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 02:31:53 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 06 Oct 2022 02:31:54 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 02:31:55 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:32:02 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 06 Oct 2022 02:32:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 02:32:03 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 06 Oct 2022 02:32:19 GMT
RUN boot
# Thu, 06 Oct 2022 02:32:19 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2152e7f09463e6c7e89c91d7854a893cfa62910bf4ac2cd6ac8b299794427865`  
		Last Modified: Thu, 06 Oct 2022 02:57:06 GMT  
		Size: 194.9 MB (194866576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad59bbd7d162da9ce204dace80536c0aae269c4364fbb3a4c8e98bf423bd8f32`  
		Last Modified: Thu, 06 Oct 2022 02:56:50 GMT  
		Size: 2.1 MB (2144485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93944b30868870f8e9f20a16a3eec6af0493a9eb84e862d5f4aa354b6b6c04ae`  
		Last Modified: Thu, 06 Oct 2022 02:56:54 GMT  
		Size: 58.8 MB (58815820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
