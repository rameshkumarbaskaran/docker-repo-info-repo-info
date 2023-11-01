## `clojure:temurin-11-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:d649cdfb98c384e77e66bab4fbfa995c54bc75bde45c34d52c49be381317f853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9c7624b5dfbc259c3df6fea2c7147ec4dd902b1201254274b3e67b3fb2d4a3d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259199441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2033d291fac96ad13021fe41401078974af436db7a703ee91ec8c169927331a6`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:10:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:17:13 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:17:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:17:14 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Nov 2023 01:17:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Nov 2023 01:17:14 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:17:20 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Nov 2023 01:17:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Nov 2023 01:17:20 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Nov 2023 01:17:38 GMT
RUN boot
# Wed, 01 Nov 2023 01:17:38 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52bf082e2f57af3aac777d96ce5e6d17154d3e9980eb8b5ffbaffaa59e38fbe`  
		Last Modified: Wed, 01 Nov 2023 01:36:16 GMT  
		Size: 145.3 MB (145266685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1a9d05a5fb80d9917a7e58b95bd82a7af477adb42577afd8dd702f26bd930a`  
		Last Modified: Wed, 01 Nov 2023 01:36:06 GMT  
		Size: 5.5 MB (5530422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243ffd243dc874d102b5ec78b7fbf5de2c93e6423913872a783c5743a2e0f615`  
		Last Modified: Wed, 01 Nov 2023 01:36:09 GMT  
		Size: 58.8 MB (58820310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2b88aa77a7cbd3f975662cacb4eb7dbfb706c7be43a32c5c5c07753413dd98bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255788362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d595d127760046d9b3162c178e85dfa6292871d1c95e1c3e867f4cf7bd6cecf`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:56:49 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:56:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 00:56:53 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 00:56:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 00:56:53 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 00:56:58 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 00:56:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 00:56:59 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 00:57:16 GMT
RUN boot
# Tue, 31 Oct 2023 00:57:16 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c4e8ef7ccc180ff3f55a838440893d12f85b3230824ad344a7d06524ac494`  
		Last Modified: Tue, 31 Oct 2023 01:17:21 GMT  
		Size: 142.0 MB (142001954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98416ee0c7296e8974cac3aa3f11f91ded8f4c1dc6672156621817eb61770d`  
		Last Modified: Tue, 31 Oct 2023 01:17:13 GMT  
		Size: 5.4 MB (5353330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edb5d8a139866e5ca8fdd4469863228d46b5431d6335a15c271dbaa35ffba5b`  
		Last Modified: Tue, 31 Oct 2023 01:17:15 GMT  
		Size: 58.8 MB (58820500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
