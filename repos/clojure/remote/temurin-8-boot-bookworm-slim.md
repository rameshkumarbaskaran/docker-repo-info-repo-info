## `clojure:temurin-8-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:c606b76c5af856697feae01857b53445f49934900eb53c19fda28d65499d1ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:702d92cd0786cfe9d9776ae30fcb35a9ae031c70d0b80339a6177975c2fb439b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195056914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368ece34815f4514d5db08dc9818a447e41400713e1c1734876f944c7f4d9a17`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:12:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:12:34 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:12:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:12:35 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:12:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:12:35 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:12:41 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:12:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:12:41 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:12:59 GMT
RUN boot
# Wed, 01 Nov 2023 01:12:59 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03a4458912287c0ab207c0861b5c68db57c420cdee0fd3fd05b400197862363`  
		Last Modified: Wed, 01 Nov 2023 01:33:15 GMT  
		Size: 103.6 MB (103585025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312406473548d5ee66e2a477005b75ef75ed3d188704c204339cd45b56666923`  
		Last Modified: Wed, 01 Nov 2023 01:33:07 GMT  
		Size: 3.5 MB (3501708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912937c60b6cdd67995507fcac216259fee950f689cdc939c84baaa82051e7c0`  
		Last Modified: Wed, 01 Nov 2023 01:33:11 GMT  
		Size: 58.8 MB (58820345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c474e8aa67ee739e3d0c897872c1791da325b5b2ed4c1c6fb2e05f56def1ba4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194014795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da48d365482d06ccd17f5cc11c93700a7f608efa4bfb83614fa69cd41e7c5e00`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:22:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 02:22:22 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 01 Nov 2023 02:22:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:22:25 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 02:22:25 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 02:22:25 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 02:22:30 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 02:22:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 02:22:31 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 02:22:48 GMT
RUN boot
# Wed, 01 Nov 2023 02:22:48 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1456740a40a5931b0447bcb842d472fd2ce5551c26816f7d692bc84052855f3f`  
		Last Modified: Wed, 01 Nov 2023 02:41:23 GMT  
		Size: 102.7 MB (102690497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735907ce56fd2d762c5992b6f18b803527c852aa55cc3aca6867ef235b9fa21d`  
		Last Modified: Wed, 01 Nov 2023 02:41:12 GMT  
		Size: 3.3 MB (3324876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2487bcf8191df4af9e8f43543902854b3e84e0985adaa14168ffbcd2e21705`  
		Last Modified: Wed, 01 Nov 2023 02:41:15 GMT  
		Size: 58.8 MB (58820303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
