## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:e5e84496e6db8a836e0b7ec5993c45c8e17976bbbfb4fa3f755daf0eb45913d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9fce21930930c9cc04323e294a47335b8845a2afb0ca441602cb9bfd6c23f977
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219824386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462bdb239bb47ef6157c372645412527b8cb9cdd2bd1405eecb3d2a02ebc0f73`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:01 GMT
ADD file:144dff349a666134b5e98a9f1c6650fd9d6e4a88a6f98857f26eb84989360b91 in / 
# Thu, 07 Sep 2023 00:21:02 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:17:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 03:17:26 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Thu, 07 Sep 2023 03:17:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 03:17:27 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 07 Sep 2023 03:17:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 03:17:27 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 03:17:33 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 07 Sep 2023 03:17:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 03:17:33 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 07 Sep 2023 03:18:21 GMT
RUN boot
# Thu, 07 Sep 2023 03:18:21 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5dea071bb9782209397443f024a630052ab7583e365894d414f1e39cd0f65025`  
		Last Modified: Thu, 07 Sep 2023 00:25:41 GMT  
		Size: 55.1 MB (55056245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01b481a024ba4d33f0e597e2fced4d71eab6fc3c8ebf663470405837b953224`  
		Last Modified: Thu, 07 Sep 2023 03:29:35 GMT  
		Size: 103.6 MB (103585059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e601bd1503c340453d6905568d706c5bfb74165c27af7cfce79239d4efc5f93`  
		Last Modified: Thu, 07 Sep 2023 03:29:27 GMT  
		Size: 2.4 MB (2362150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a76cb88a9f95dca551722a92b74dce4529bb21d959432c61b32085dd732e21`  
		Last Modified: Thu, 07 Sep 2023 03:29:30 GMT  
		Size: 58.8 MB (58820932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6846976e030888d28823b65f9ae8da0f101a580232bad5bb703e4f80168fde42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217567140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4656ce5f46953a4ae7608beaa9b8a07db51c6a643930319e2ed6ef0ca4941e54`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 01:46:16 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 16 Aug 2023 01:46:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 01:46:18 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 16 Aug 2023 01:46:18 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 01:46:18 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 01:46:23 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 16 Aug 2023 01:46:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 01:46:24 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 16 Aug 2023 01:46:42 GMT
RUN boot
# Wed, 16 Aug 2023 01:46:42 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73e72ffee157aface2093ca7b44ca1e9d7d8010e8b3344c5760c1ae633be3d0`  
		Last Modified: Wed, 16 Aug 2023 01:56:15 GMT  
		Size: 102.7 MB (102690463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b7cda0152fc848681cfcb2e8d7e2d37db6cbf6d054d4d78c77730b6f60e28e`  
		Last Modified: Wed, 16 Aug 2023 01:56:08 GMT  
		Size: 2.4 MB (2351417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff4bd27505dabeddc455a9f49259b9f5b2b7b656f3b871f7f0def2cc5a57a21`  
		Last Modified: Wed, 16 Aug 2023 01:56:11 GMT  
		Size: 58.8 MB (58820481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
