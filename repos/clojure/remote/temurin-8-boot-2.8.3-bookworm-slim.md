## `clojure:temurin-8-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:d430ff2bcdb6e39726eb870bd9c595267802bcc750649915fd93d26d1e9d801c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ff2d01c5ba9a345882ecbd70f6a514bcd95c37ae607293b9a3caf063eddfbb55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195056835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae79c7add8a4c9e0bd25a77efc36b49fc14a2318374158d672e2081a9ad5170c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:28:08 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:28:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:28:09 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 01:28:09 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:28:09 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:28:15 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 01:28:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:28:15 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 01:28:34 GMT
RUN boot
# Fri, 13 Oct 2023 01:28:34 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d25ccb95233478198757a427ee2f81fab3092542dec1b3fbcd1c703e7241ae`  
		Last Modified: Fri, 13 Oct 2023 01:44:37 GMT  
		Size: 103.6 MB (103585059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f348e226c74187b54e2bb88299c3e222cf23d2822cc183945a598cff60e62666`  
		Last Modified: Fri, 13 Oct 2023 01:44:29 GMT  
		Size: 3.5 MB (3501451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25df56ec65bb24937b03cae9278bcb13bbf8e6ab575ad3e9d3231a6b88c64727`  
		Last Modified: Fri, 13 Oct 2023 01:44:32 GMT  
		Size: 58.8 MB (58820451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b7918ab93b59b53fd4bc6527874c21c63d23eca545c145d7ae617073942c86c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194015507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8b80b0c81cb079a2b42591660b3ccfbe986e86da16140a9e5776f86a729c4c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 00:59:52 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Fri, 13 Oct 2023 00:59:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 00:59:54 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 00:59:54 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 00:59:55 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:00:00 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 01:00:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:00:00 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 01:00:18 GMT
RUN boot
# Fri, 13 Oct 2023 01:00:18 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57b690f142bf71ee0e56d780ce627f1f5444df7e8057dfc8cd7d677acefac58`  
		Last Modified: Fri, 13 Oct 2023 01:13:33 GMT  
		Size: 102.7 MB (102690507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4550d7dc89d2d835d6455e43607cc51093c5ceb23f61bf0cb7008015e1b467`  
		Last Modified: Fri, 13 Oct 2023 01:13:26 GMT  
		Size: 3.3 MB (3325261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f90346679663027ca1228130ebdbf0858ca60bb2c80ca33d5172f3ae68c392`  
		Last Modified: Fri, 13 Oct 2023 01:13:29 GMT  
		Size: 58.8 MB (58820455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
