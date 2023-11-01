## `clojure:temurin-8-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:c44d75723fc06c0599346ecb00e7489e93377505b874291349fafe60c7c2e77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bookworm-slim` - linux; amd64

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
