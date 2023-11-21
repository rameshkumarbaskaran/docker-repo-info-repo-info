## `clojure:temurin-11-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:77915f0f62b3189d1fbff0db4bdc438b8209977b81caddddbd681d6ceb0bd3d9
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
$ docker pull clojure@sha256:37866811476c0c9d0fcdcb0ec0c19cc005e2ef80fbc5bf0654801a05bb00900e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255788142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4217de0df9447c7d0e8aeefffef3bc1d0702b0cf3f06fe81636e77811c748b88`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:26:16 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:26:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 07:26:19 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Nov 2023 07:26:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Nov 2023 07:26:20 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 07:26:25 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Nov 2023 07:26:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Nov 2023 07:26:25 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Nov 2023 07:26:42 GMT
RUN boot
# Tue, 21 Nov 2023 07:26:42 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354d327993bf126405e169db138848ddbbe9f7b0434cc3fbc3132a2dafcb3ed1`  
		Last Modified: Tue, 21 Nov 2023 07:43:01 GMT  
		Size: 142.0 MB (142001937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be0125d46d180a3603fd23a37a8221e66e907958cd5d4cfad68b5e03efc11f3`  
		Last Modified: Tue, 21 Nov 2023 07:42:53 GMT  
		Size: 5.4 MB (5353207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32011ac7d4214e71c27fe34d41d7bd6cc74e12b7af98aa8bbc83393bc426463`  
		Last Modified: Tue, 21 Nov 2023 07:42:55 GMT  
		Size: 58.8 MB (58820348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
