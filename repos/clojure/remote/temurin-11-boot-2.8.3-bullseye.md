## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:d31e3bbf8b5b83c8e954faa411f9279b339d674cd296ded770881a5d87f26a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e24a2498ff003ba45f033d020aeea2239234ae7662b0536eaccaa335dde5e6f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314353783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6583b6f530045d8ff226771fdca6d424b96fe5173a84b6c5c9b17f8c542f8da1`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:10:35 GMT
COPY dir:24028fba84faa85b57bc32be14abf8fad6a4bd4db557cb5499b6d5cf38d97646 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:10:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:10:37 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Nov 2022 20:10:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Nov 2022 20:10:38 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:10:46 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 02 Nov 2022 20:10:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Nov 2022 20:10:46 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Nov 2022 20:11:06 GMT
RUN boot
# Wed, 02 Nov 2022 20:11:06 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcd28620e58cb67f5c8f9e27eae0508ebb1bd7db0a5e05838b142166ca46960`  
		Last Modified: Wed, 02 Nov 2022 20:24:27 GMT  
		Size: 198.1 MB (198124725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e9b5900738af25c3979e5d3f4500c111d0d43ff08f86e8561d669b05cd9031`  
		Last Modified: Wed, 02 Nov 2022 20:24:13 GMT  
		Size: 2.4 MB (2362175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d4512422418d78bfea33689c483d5cb1c533cfd5d89013e278a5fbe2a7a287`  
		Last Modified: Wed, 02 Nov 2022 20:24:19 GMT  
		Size: 58.8 MB (58820551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8fcb2d75a809dfe62ab170d98964ccdb084634b0baea4c23ccd0d5aad0c9403c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309742379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24facec935901af7560f7c2a8feda0d5229b0520c3ed2c2e0d3f245fb5132823`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:46:38 GMT
COPY dir:e48336735658172388295f760b71f5f10a9b7d3f960c6e4546718a38dd6452e7 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:46:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:46:42 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Nov 2022 20:46:42 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Nov 2022 20:46:42 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:46:48 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 02 Nov 2022 20:46:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Nov 2022 20:46:49 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Nov 2022 20:47:06 GMT
RUN boot
# Wed, 02 Nov 2022 20:47:06 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea5981601b157d45e631f4fdac4fdd41f2d6daaa8c619fc62dfe32805bfb784`  
		Last Modified: Wed, 02 Nov 2022 20:58:15 GMT  
		Size: 194.9 MB (194867680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1dfc7d6fa2ae0c78d62dc37f0cd1d5073e4883d4af1626a3d5b2834ca180ca`  
		Last Modified: Wed, 02 Nov 2022 20:58:04 GMT  
		Size: 2.4 MB (2352303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0546f67fb8d06ce72732d1b7812d05d0933b9532df3cd5a4e11bf4f3e40da1`  
		Last Modified: Wed, 02 Nov 2022 20:58:07 GMT  
		Size: 58.8 MB (58820430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
