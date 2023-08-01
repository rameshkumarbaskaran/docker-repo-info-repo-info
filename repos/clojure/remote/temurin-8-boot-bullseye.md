## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:9c5ccf427741341a5994b42b6b4ebeca8b50be6eb388adc416956c670f7f4f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:62795195c469386772e3aa4a59c49329ff643a8a43366cc40299a64ab1234624
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219823341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1f23e7c60ce685c2e8b2841f043a4ba011115c2b57faca2e45976c08ba3074`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:55 GMT
ADD file:b493776b6d91132ce50735e2d82076620774a1e0a690cf96777ddd6b85f513ef in / 
# Thu, 27 Jul 2023 23:24:55 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:13:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 01 Aug 2023 22:04:20 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Tue, 01 Aug 2023 22:04:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:04:21 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 01 Aug 2023 22:04:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 01 Aug 2023 22:04:21 GMT
WORKDIR /tmp
# Tue, 01 Aug 2023 22:04:27 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 01 Aug 2023 22:04:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 01 Aug 2023 22:04:27 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 01 Aug 2023 22:04:54 GMT
RUN boot
# Tue, 01 Aug 2023 22:04:54 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:9a9e034800a1747ea288f38f6087c036acac99dd3ec5255bf7798abd8c23a304`  
		Last Modified: Thu, 27 Jul 2023 23:29:45 GMT  
		Size: 55.1 MB (55055571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5994baf91037b8621fd988336f98795e08c9c32f2a733406596f429bf2ee92`  
		Last Modified: Tue, 01 Aug 2023 22:15:16 GMT  
		Size: 103.6 MB (103585038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d13bf65ff8c79ee1b12ba130618c2e0040e6556324cbad564dcd19adcc0a00`  
		Last Modified: Tue, 01 Aug 2023 22:15:07 GMT  
		Size: 2.4 MB (2362137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7502f883c7ed1cd0b983600d5c813cce3b22c922f32cd28fb70dbdb54ddc2ef4`  
		Last Modified: Tue, 01 Aug 2023 22:15:12 GMT  
		Size: 58.8 MB (58820595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:59343fc07aa6d5aafe37008c146cbb0d0a65df5524577f2da6788944ce1cef8d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217566971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee83b04c0c8c9d4353d2ed8ea3a9eaed4690f8aa173d3e4befca491170fe846`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 01 Aug 2023 22:10:28 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Tue, 01 Aug 2023 22:10:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 22:10:31 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 01 Aug 2023 22:10:31 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 01 Aug 2023 22:10:31 GMT
WORKDIR /tmp
# Tue, 01 Aug 2023 22:10:36 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 01 Aug 2023 22:10:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 01 Aug 2023 22:10:36 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 01 Aug 2023 22:10:54 GMT
RUN boot
# Tue, 01 Aug 2023 22:10:55 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c068dad8acfadc68ead3eb00398372dcec29fed6a09eca2f88f82eca8ecd10`  
		Last Modified: Tue, 01 Aug 2023 22:18:11 GMT  
		Size: 102.7 MB (102690458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3ffefcf00cb07d8a3e73a9dedef91dcd2a4305c18274b5318ebe37df85a168`  
		Last Modified: Tue, 01 Aug 2023 22:18:04 GMT  
		Size: 2.4 MB (2351403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ea7c20bd7cb8d6590628a7b910fa72283c79ac81c1108d6ed19f46446ce6f6`  
		Last Modified: Tue, 01 Aug 2023 22:18:07 GMT  
		Size: 58.8 MB (58820320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
