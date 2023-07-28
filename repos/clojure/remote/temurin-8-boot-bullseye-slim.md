## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:7faa2f5d7e2b9fd8d213a44efea483e5ebc3d205b980b0dd9d38a58c80f2061a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:71fdff0f1eab1e96775925b78aa0a31f4ec2c76fd4e5eac7bcef8f663da41aef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145957724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1925ae99c9919877f5331b78f976c0b67874341dfc869e71e5df36287a8cb3`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 03:14:47 GMT
COPY dir:715eb4123a1bd94a1f232c902a6f3cdcc4011195a3e566c0f0ddc35dd1e83095 in /opt/java/openjdk 
# Fri, 28 Jul 2023 03:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 03:14:47 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 28 Jul 2023 03:14:48 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 28 Jul 2023 03:14:48 GMT
WORKDIR /tmp
# Fri, 28 Jul 2023 03:14:53 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 28 Jul 2023 03:14:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 28 Jul 2023 03:14:53 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 28 Jul 2023 03:15:12 GMT
RUN boot
# Fri, 28 Jul 2023 03:15:12 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ba5371a0abebe830bcea6b9222d076c8228ded98370c272f71596d172e2a49`  
		Last Modified: Fri, 28 Jul 2023 03:28:13 GMT  
		Size: 54.6 MB (54642102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ee254c577f2d981a17fe81a1627f2ae3158b8237e058870edf410f064591dd`  
		Last Modified: Fri, 28 Jul 2023 03:28:06 GMT  
		Size: 1.1 MB (1077548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98590bbb5b46c3eafe41e7443b46318c587d2e74755dff4c4fe7c4dfbc080aeb`  
		Last Modified: Fri, 28 Jul 2023 03:28:10 GMT  
		Size: 58.8 MB (58820472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2c96a508b50a67105a84d5beae5eeda3df8a1fedeb0ea42eda5e8c4db11f783
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143691003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069bec405ad299afd83c8232feccae80d9321e6684af9a808489ffc2cf80fdf2`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:44:12 GMT
COPY dir:f6bbe63c81e220d954915791686219263d8c45918fd81b238f7c9f6b21f076f8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:44:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:44:13 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 04 Jul 2023 06:44:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 04 Jul 2023 06:44:13 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 06:44:18 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 04 Jul 2023 06:44:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Jul 2023 06:44:18 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 04 Jul 2023 06:44:36 GMT
RUN boot
# Tue, 04 Jul 2023 06:44:37 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b2f40633878980b926bd5c39f216162f482779ac62dfe05a4cac4558cd3356`  
		Last Modified: Tue, 04 Jul 2023 06:53:48 GMT  
		Size: 53.7 MB (53742698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2309eeb9dfd8fef77e4f5dcf3108410d58724574a8a8858af1bbdf84760089`  
		Last Modified: Tue, 04 Jul 2023 06:53:53 GMT  
		Size: 1.1 MB (1064794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b6a22a96e076ccf1330dac1b58b86017439a1ff0ec93a0b946b8fb38a0951d`  
		Last Modified: Tue, 04 Jul 2023 06:53:46 GMT  
		Size: 58.8 MB (58820554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
