## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:fd729b7de5c51c3f325887755f231ce63a137d350de0969a75ccc623e02c40e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4e56041cb7848f901ee8a212c3d8c5ac74ebb8bbd90229bd018d6c1b9369efc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261067780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8625a1ce294031278e7da08e4229b2d4b484f20c81c71602562da3720551ec`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:55 GMT
ADD file:b493776b6d91132ce50735e2d82076620774a1e0a690cf96777ddd6b85f513ef in / 
# Thu, 27 Jul 2023 23:24:55 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:13:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 03:17:02 GMT
COPY dir:2fc258758bb2c25982e4c8348cffe5a1ab54f4c54e52ff852a817cdf5bd62215 in /opt/java/openjdk 
# Fri, 28 Jul 2023 03:17:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 03:17:03 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 28 Jul 2023 03:17:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 28 Jul 2023 03:17:03 GMT
WORKDIR /tmp
# Fri, 28 Jul 2023 03:17:08 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 28 Jul 2023 03:17:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 28 Jul 2023 03:17:09 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 28 Jul 2023 03:17:27 GMT
RUN boot
# Fri, 28 Jul 2023 03:17:27 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:9a9e034800a1747ea288f38f6087c036acac99dd3ec5255bf7798abd8c23a304`  
		Last Modified: Thu, 27 Jul 2023 23:29:45 GMT  
		Size: 55.1 MB (55055571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df166fc4715d337f554c5b6904774af766db5e850d3500e12eeafae147f25b5`  
		Last Modified: Fri, 28 Jul 2023 03:29:39 GMT  
		Size: 144.8 MB (144829492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2782dd0817ff7e751ac7cd7df09cc33a27a370534e24fee77783e54db7141dc6`  
		Last Modified: Fri, 28 Jul 2023 03:29:28 GMT  
		Size: 2.4 MB (2362154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e460839bb1b401df6827b07db7e0ed6f07eabe288406ea41a9d077b1bb1b73ee`  
		Last Modified: Fri, 28 Jul 2023 03:29:31 GMT  
		Size: 58.8 MB (58820563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2249e9fb7909d950c7577c7f4f8adcbe7b7a41a90342bd8bf6b13efb92f59977
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256441215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201e691361556a9a6b136d714fe1bd23bb68b13a8228b0ac58fe91ab2c898bf0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:43:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Jul 2023 01:07:04 GMT
COPY dir:e71da8247d58ed4b0dfbf219951c863c79ac94b7f45cb60320ea827dfa699275 in /opt/java/openjdk 
# Wed, 26 Jul 2023 01:07:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:07:07 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Jul 2023 01:07:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Jul 2023 01:07:08 GMT
WORKDIR /tmp
# Wed, 26 Jul 2023 01:07:13 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Jul 2023 01:07:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Jul 2023 01:07:13 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Jul 2023 01:07:32 GMT
RUN boot
# Wed, 26 Jul 2023 01:07:33 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a099a46124988665742eae84cd51e5a2ec69ba12a5a0324bfdecb15c9fcca0ec`  
		Last Modified: Wed, 26 Jul 2023 01:13:29 GMT  
		Size: 141.6 MB (141565305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b34da4dc58b8551e76f9c5e3c916466191bf7ac36466592eabfa5fc42b738c`  
		Last Modified: Wed, 26 Jul 2023 01:13:20 GMT  
		Size: 2.4 MB (2351394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f357330e1bb51be8f74c4f777503bc25b17ba6494113f8c22da6676ec2c430`  
		Last Modified: Wed, 26 Jul 2023 01:13:22 GMT  
		Size: 58.8 MB (58820537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
