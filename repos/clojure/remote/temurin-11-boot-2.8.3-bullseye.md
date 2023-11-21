## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:be04ea75198408b398cf73df368ca49e8635a028f79abac7c9985f0622a91490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:70cf2741fc116acff506cd79650a95287e906b763f8eedc1e5bfa64e368fab34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261513653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7fba3f89a7a879fae76ff157a4157abde978c0f61b1a03d4842bfbd1ba431d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:14:43 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 21 Nov 2023 10:14:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 10:14:44 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 10:14:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 10:14:44 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 10:14:49 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 10:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 10:14:50 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 10:15:06 GMT
RUN boot
# Tue, 21 Nov 2023 10:15:06 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe902143c3fd99b4ac9a0291a2832730d347def235a791db08e9e5f1c82f26a`  
		Last Modified: Tue, 21 Nov 2023 10:32:35 GMT  
		Size: 145.3 MB (145266698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef5d38aa19bed21dac754717ba7e6b148a33262d5cc337d76520834921cbfb5`  
		Last Modified: Tue, 21 Nov 2023 10:32:24 GMT  
		Size: 2.4 MB (2368671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9dfe129b5aac900a6feb2318905f774d2dc4c2a3681d08a5123f2b59534b38`  
		Last Modified: Tue, 21 Nov 2023 10:32:27 GMT  
		Size: 58.8 MB (58820381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:09ff869ec2332a35f2058ba224819ed8300dfdabefb8c97a583284e5bb96b6d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256887672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d11dc8a136aff235a1de48ef2f2abc073e9306dd27e678b7b9e67faabc531f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:27:16 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:27:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 07:27:19 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 07:27:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 07:27:20 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 07:27:24 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 07:27:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 07:27:24 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 07:27:41 GMT
RUN boot
# Tue, 21 Nov 2023 07:27:41 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55c92be40caea1a03c3b8373d2ab9d08188bb25df2b9a9abc8e846cc50c348f`  
		Last Modified: Tue, 21 Nov 2023 07:43:36 GMT  
		Size: 142.0 MB (142001943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c5c048592f5c7d52ca492941f2f1e690bcd7d9e2c9d91026820d3cc6a14cb`  
		Last Modified: Tue, 21 Nov 2023 07:43:28 GMT  
		Size: 2.4 MB (2357435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1645c15e5a149a30561763dde1d9a2672336ead58170b87133317f3e6d63970`  
		Last Modified: Tue, 21 Nov 2023 07:43:30 GMT  
		Size: 58.8 MB (58820422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
